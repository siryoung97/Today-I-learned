# socket 

## socket 정의
 소켓은 컴퓨터 네트워크에서 서로 두게의 프로세스 가  통신을 할수있도록 양족에 생성 되는링크의 단자입니다  

## socket 하고 tcp/ip 하고 포트의 관계 
 tcp 에서 IP 주소  하고 포트주소 로 구성되있 주소를 소켓에 bind 하면서 각각의 주 소에 유일한 소켓을 할당해줍니다. 이제 서로 다른 두개의 프로세스가 통신을 할때   소켓 을 이용해 상대방을 찻아 통신합니다. 

## socket 을 코드로 구현하기 
 일단 소켓을 구현하기 위해서 server 하고 client 을 구분해야합니다. 대부분 client 가 요청하면 server 가 요청을 받아주면서 서로가 연결되는 방식입니다. 이때 golang 에서는 net.dial, net.listen 그리고 net.accept 라는 함수를 을 이용해 구현됩니다. 주로 client 에서 net.dial 을 이용하고 server 에서 net.listen 하고 accept 을 이  용합니다. net.dial 을 주소를 보내 연결을 요청하고 net.listen 은 주소가 맛는지   그리고 중복 여부를 확인하고 문제가 없으면 accept 함수를 통해 연결을 구축합니다.          

 
