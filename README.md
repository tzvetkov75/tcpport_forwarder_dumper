
This is very small java program that helps you to troubleshoot HTTP, SOAP or RESTful Web services on machines where you do not have root privileges (pcap, tcpdump, wireshark)

It makes two things:

   1) Local port forwarding to remote host and port, like  local port 8080 to www.google.com:80

   2) Dumps in in and out messages (datagrams) to the standard out (stdout)

This is not performance tool! It helps to understand what is going over the network, if you do not have root privileges for pcap, tcpdump, wireshark etc.

usage: 

	In the build folder you will find the jar

java -jar tcpport_forwarder_dumper.jar [local-port] [remote-host]:[remote-port] 

Example:

$ java -jar tcpport_forwarder_dumper.jar 8080 www.google.com:80

TCP Port forwarding - content logger (dummper to stdout) v0.1 vesselin
listen on local port 8080
Forwarding to www.google.com:80
TCP Forwarding 127.0.0.1:49793 <--> 216.58.211.36:80 started.
------- DATAGRAM ------------
GET http://www.google.com
------- DATAGRAM ------------
HTTP/1.0 302 Found
Cache-Control: private
Content-Type: text/html; charset=UTF-8
Location: http://www.google.ch/?gfe_rd=cr&ei=51shVrreONSo8weigLKQBg
Content-Length: 258
Date: Fri, 16 Oct 2015 20:19:51 GMT
Server: GFE/2.0

<HTML><HEAD><meta http-equiv="content-type" content="text/html;charset=utf-8">
<TITLE>302 Moved</TITLE></HEAD><BODY>
<H1>302 Moved</H1>
The document has moved
<A HREF="http://www.google.ch/?gfe_rd=cr&amp;ei=51shVrreONSo8weigLKQBg">here</A>.
</BODY></HTML>

TCP Forwarding 127.0.0.1:49793 <--> 216.58.211.36:80 stopped.
 

  
