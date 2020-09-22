<div align="center">

## Chat Without IP Knowledge


</div>

### Description

Wanna know how to connect a client and a server via winsock without the other person having to know your IP???
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[N/A](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/empty.md)
**Level**          |Intermediate
**User Rating**    |3.5 (39 globes from 11 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[Internet/ HTML](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/internet-html__1-34.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/chat-without-ip-knowledge__1-11443/archive/master.zip)





### Source Code

```
The way to do this is to go to a URL Redirection website... www.cjb.net is a good one. Create an account there, it's free, and put your current IP number in the box that asks you for your homepage. If your IP is 12.34.567.89, then you would put HTTP://12.34.567.89:80 in the box. Since 80 is what is normally used for HTML, it's better to use it here. Continue creating the account and there you go.
Now, the client's program will have a winsock control and a web browser control on their form. When they click the command button to connect, the code will tell the web browser to go to the url... http://myip.cjb.net, or whatever you created. Of course, the winsock control on your end will be listening for connections. When the client has done his/her job by clicking the command button to connect, it will send their IP to you. You retrieve this IP by putting the ACCEPT RequestID routine in the Winsock_ConnectionRequest event, and then using the RemoteHostIp to then connect to their computer. It is much easier to have the client's program have 2 winsock controls on their form... 1 for connecting to http://whatever.cjb.net, and 1 for listening for YOUR connection request. The winsock control that connects to the internet requires no IP input, nor PORT number. The winsock control that allows YOU to connect to THEM will be a different port, so the ports don't conflict.
The client doesn't have to know the IP number, nor do you. The only thing you, the server, has to do before the client connects is modify the CJB.NET account with your current IP number before the client connects. If you have a DSL or better, or a static IP, you won't have to mess with modifying your CJB.NET account to add your new IP.
And there you have it. I hope this has helped some of you out. And if you have any comments suggesting that this doesn't work, I have made several programs that do this... and I've had 0 problems.
One more thing, feedback is always welcome. Even if you have something negative to say. Please vote.
```

