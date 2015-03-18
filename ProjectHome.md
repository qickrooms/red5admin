# RED5 INTRO #
Red5 is an open source java solution for Video on Demand and sync remote client applications.
It is the result of a reverse engineering  translation of RTMP protocol that Flash Media Server implements.
More information about the project could be found at http://www.osflash.org/red5
Red5 community is growing faster and faster every day. There are many blogs and forum which deal with applications built on Red5 platform; furthermore many developers write open source solution for it.


## WHY TO WRITE AN ADMIN PANEL ##
The need of a developer admin panel grows every time you have to implement big application for Red5.
One of the big leaks between red5 and FMS is indeed the admin panel.

Thinking about it and searching  the web I found a simple, but well made, admin panel for red5, with many runtime information such as clients connected, used bandwidth…

I real think that it’s not enough for a developer; a developer may need something more like a debugger… so … voilà : )
This is the first step for a real Red5 Admin Panel

<br><br>


<img src='http://www.okpress.it/red5Admin/objectInspector.jpg' />

<h1>FEATURES</h1>


<ul><li>List Application instances<br>
</li><li>List Shared Object in scope<br>
</li><li>Inspect Shared Object properties<br>
<ul><li>List Arrays<br>
</li><li>List custom Object<br>
</li><li>List primitive types<br>
</li></ul></li><li>Stream inspector<br>
<ul><li>list available recorded streams<br>
</li><li>list live streams<br>
</li><li>stream preview</li></ul></li></ul>


<h1>Project structure</h1>

the project is structured in two parts :<br>
<ul><li>Server Side application<br>
</li><li>Flex Client Application</li></ul>

<h2><a href='.md'>Client SIDE </a></h2>
Red5 Admin Panel is a Flex project written respecting Adobe Cairngorm MVC structure<br>
<br>
<br>
<h2><a href='.md'>Server SIDE </a></h2>
For the server side, the Admin Panel, is a normal web application and you have to put it in red5 webapp folder.<br>
In my case the path is C:\Programmi\Red5\webapps\red5Admin<br>
In our server side application we can simply add our security policy that depends on the connection request from the client.<br>
It is not current implemented and it will be in the next release.<br>
<br>
<br>
<h2><a href='.md'>RED5 PATCH </a></h2>
One on the purpose of the Flex Client inspector is to list and preview all the streams available on the server. To do that it need to play streams that can be on a different scope so I had to modify two red5 files. in patch.zip you can find the files; please copy them in src red5 folder<br>
<br>
<h2><a href='FUTURE.md'>IMPLEMENTATIONS </a></h2>
TODO<br>
