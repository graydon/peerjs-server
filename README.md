# PeerJS Server: Server component for PeerJS #

PeerServer helps broker connections between PeerJS clients. Data is not proxied through the server.

##[http://peerjs.com](http://peerjs.com)


**If you prefer to use a cloud hosted PeerServer instead of running your own, [sign up for a free API key here](http://peerjs.com/peerserver)**


### Run PeerServer

Install the library:

    npm install peer

Run the server:

    var PeerServer = require('peer').PeerServer;
    var server = new PeerServer({ port: 9000 });

Connecting to the server from PeerJS:

    <script>
        // No API key required when not using cloud server
        var peer = new Peer('someid', {host: 'localhost', port: 9000});
    </script>

Using HTTPS: Simply pass in PEM-encoded certificate and key.

    var fs = require('fs');
    var PeerServer = require('peer').PeerServer;

    var server = new PeerServer({
      port: 9000,
      ssl: {
        key: fs.readFileSync('/path/to/your/ssl/key/here.key'),
        certificate: fs.readFileSync('/path/to/your/ssl/certificate/here.crt')
      }
    });

## Problems?

Discuss PeerJS on our Google Group:
https://groups.google.com/forum/?fromgroups#!forum/peerjs

Please post any bugs as a Github issue.
