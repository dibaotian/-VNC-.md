
#### 通过Xserver 打开Firefox实在是太慢了

### step1 在local destop  map port to jump server
   ssh -L 5975:localhost:5901 <jump_server_user>@<jump_server_ip> -X
   it will let you login to jump server
   
### setp2 in the jump server map port to backend server
   ssh -L 5905:localhost:5975 <backend_server_user>@<backend_server_ip> -X
   it will let you login to backend server

### step3 enable vncserver in the backend server
   vncserver -geometry 1920x1080
   
   
### setp4 in the local desktop user the vnc client login (though pot 5905)
  localhost:5905
