
This is very small java program that helps you to troubleshoot HTTP, SOAP or RESTful Web services on machines where you do not have root privileges (pcap, tcpdump, wireshark)

It makes two things:

   1) Local port forwarding to remote host and port, like  local port 8080 to www.google.com:80

   2) Dumps in in and out messages (datagrams) to the standard out (stdout)

This is not performance tool! It helps to understand what is going over the network, if you do not have root privileges for pcap, tcpdump, wireshark etc.

usage: 

java -jar tcpport_forwarder_dumper.jar [local-port] [remote-host]:[remote-port] 

the jar is in the build folder

Example:

$ java -jar tcpport_forwarder_dumper.jar 8080 www.google.com:80

TCP Port forwarding - content logger (dummper to stdout) v0.1 vesselin
listen on local port 8080
Forwarding to www.google.com:80
TCP Forwarding 127.0.0.1:49793 <--> 216.58.211.36:80 started.
------- DATAGRAM ------------
GET http://www.google.com
------- DATAGRAM ------------
&lt;HTML&gt;&lt;HEAD&gt;&lt;meta http-equiv=&quot;content-type&quot; content=&quot;text/html;charset=utf-8&quot;&gt;<br/>&lt;TITLE&gt;302 Moved&lt;/TITLE&gt;&lt;/HEAD&gt;&lt;BODY&gt;<br/>&lt;H1&gt;302 Moved&lt;/H1&gt;<br/>The document has moved<br/>&lt;A HREF=&quot;http://www.google.ch/?gfe_rd=cr&amp;amp;ei=51shVrreONSo8weigLKQBg&quot;&gt;here&lt;/A&gt;.<br/>&lt;/BODY&gt;&lt;/HTML&gt;

TCP Forwarding 127.0.0.1:49793 <--> 216.58.211.36:80 stopped.
 

  
