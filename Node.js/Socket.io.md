
#### Basic server setup

```javascript
const app = require("express")();
// creating server
const server = require("http").createServer(app);
// initializing socket io with http server
const io = require("socket.io")(server, {
  cors: {
    origin: "*",
  },
});

server.listen(8000, () => console.log("server is running on 8000.."));
```

#### Listening for connections

```javascript
io.on("connection",(socket)=>{
  console.log(socket)
})
```

#### Listen events

```javascript
io.on("connection",(socket)=>{
  socket.on("send",(payload)=>{
    conssole.log(payload)
  })
})
```

#### Emit events

```javascript
io.on("connection",(socket)=>{
  socket.emit("send",{name:"piyush"})
  
  // user this when you want to emit the message to all the users except you
  socket.broadcast.emit("send",{name:"piyush"})
})
```

#### Socket Disconnect

```javascript
io.on("connection",(socket)=>{
   // triggres when user disconnect
  socket.on("disconnect", (payload) => {
   
  });
})
```