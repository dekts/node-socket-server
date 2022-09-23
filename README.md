# node-socket-server
An independent socket IO server has been created to handle events from both servers and clients in a bidirectional manner

### Installation

```
npm i && node index.js
```

### How to use this server in another apps

Add below code in your view file to test.

```js
<script src="https://code.jquery.com/jquery-3.6.0.js" integrity="sha256-H+K7U5CnXl1h5ywQfKtSj8PCmoN9aaq30gDh27Xc0jk=" crossorigin="anonymous"></script>
<script src="https://cdn.socket.io/4.0.1/socket.io.min.js" integrity="sha384-LzhRnpGmQP+lOvWruF/lgkcqD+WDVt9fU3H4BWmwP5u5LTmkUGafMcpZKNObVMLU" crossorigin="anonymous"></script>

<script>
    $(function() {
        let ip_address = 'localhost';
        let socket_port = '3000';
        let socket = io(ip_address + ':' + socket_port);

        socket.on('add-to-board', (message) => {
            console.log(message);
        });
    });
</script>
```
