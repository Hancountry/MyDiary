# 프로젝트 명: MyDiary
## 발표영상 링크: https://youtu.be/Rw7BHSdrxsQ 

목적: 캘린더 뷰를 사용한 일기장 만들기

구현한 기능: 달력 날짜를 입력받아 저장된 일기 불러오기, 새로운 일기 작성하기, 수정, 삭제 기능. 

파일을 생성하여 파일 안에 일기를 저장함. 파일을 읽어서 일기가 저장된 날짜는 해당 일기를 보여줌.

  public void  checkDay(int cYear,int cMonth,int cDay){
  
 fname=""+cYear+"-"+(cMonth+1)+""+"-"+cDay+".txt"; //저장할 파일 이름설정
        
        FileInputStream fis=null; //FileStream fis 변수
        
        try{
            fis=openFileInput(fname);

            byte[] fileData=new byte[fis.available()];
            fis.read(fileData);
            fis.close();

            str=new String(fileData); 
            // 파일을 읽는 메소드 
            
버튼이나 입력칸과 같은 요소들을 invisible로 설정해놓고 상황에 맞게 화면에 띄움.
            
             calendarView.setOnDateChangeListener(new CalendarView.OnDateChangeListener() {
            @Override
            public void onSelectedDayChange(@NonNull CalendarView view, int year, int month, int dayOfMonth) {
                diaryTextView.setVisibility(View.VISIBLE);
                save_Btn.setVisibility(View.VISIBLE);
                contextEditText.setVisibility(View.VISIBLE);
                textView2.setVisibility(View.INVISIBLE);
                cha_Btn.setVisibility(View.INVISIBLE);
                del_Btn.setVisibility(View.INVISIBLE);
                diaryTextView.setText(String.format("%d / %d / %d",year,month+1,dayOfMonth));
                contextEditText.setText("");
                checkDay(year,month,dayOfMonth);
            }
        });
- 초반에 기획했을 당시 9개의 표정 버튼을 만들어서 기분을 기록하는 일기장을 만들고 싶었으나 실력이 미흡한 나머지 알 수 없는 오류들이 많아졌습니다. 
      고치려고 많이 노력했는데 건들면 건들수록 더 악화되기만해서 가장 기본만 남기게 되었습니다.. 앞으로 더 열심히 공부하겠습니다 죄송합니다
      
![angry](https://user-images.githubusercontent.com/95368466/146389079-dcff1c78-c5f1-4e9f-836c-70c781caca2a.jpeg)
삽입하려 했던 버튼 이미지 중 하나입니다.


      
      
            
