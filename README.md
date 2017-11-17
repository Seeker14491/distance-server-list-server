# Distance Server List Server

This is a server that polls [Distance](http://survivethedistance.com/)'s lobby list, and serves the data as JSON through HTTP. It's implemented as a Unity project in order to have access to the same APIs Distance uses to query servers.

##### Example JSON returned

```json
{"servers":[{"build":5465,"connectedPlayers":1,"mode":"Sprint","passwordProtected":true,"playerLimit":24,"serverName":"Seekr's server"}]}
```



#### Building and Usage

The project should build in Unity without any additional configuration. Once the executable is running, the server will respond to HTTP requests with the server list. You can check if it's working by going to [http://localhost/](http://localhost/) in a web browser on the same computer.



##### Running headless

It should be possible to run the executable without it creating a useless window and on computers with no GPU by passing it the  `-batchmode -nographics` flags. Linux builds alternatively have a headless mode toggle in the build settings. I haven't tried any of this though.

![headless mode toggle](https://noobtuts.com/content/unity/unet-server-hosting/build_headless_mode.png)