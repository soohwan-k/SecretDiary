# SecretDiary
sharedPreference  
->commit: UI thread를 블록하고 데이터를 저장할 때 까지 기다림   
->apply: 기다리지 않고 비동기적으로 저장  

UI thread를 블록한다는 것은 이 작업이 끝날 때 까지 ui가 동작하지 않고 잠깐 멈춤  
따라서 너무 무거운 작업을 할 수 없기 때문에 apply를 통해 저장하는 것이 좋음
  
    
Handler: thread와 thread간의 통신을 엮어주는 안드로이드에서 제공하는 기능  
평소에 사용하는 thread는 main thread  
main thread가 느려지는 네트워크 통신, 파일 저장 등의 작업을 할 때 별도로 thread를 열어서 작업  
