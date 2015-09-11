# Chat app written in node.js and socket.io

## Libraries used
<ul>
  <li>node.js / npm</li>
  <li>socket.io</li>
  <li>express</li>
  <li>node-uuid</li>
  <li>underscore</li>
  <li>ejs</li>
</ul>

## Setup and configuration

Make sure that you update <strong>server.js</strong>:
<pre>server.listen(app.get('port'), function(){
  console.log('Express server listening on port ' + app.get('port'));
});</pre>
and add your own IP address/hostname if required, i.e.:
<pre>server.listen(app.get('port'), "192.168.1.93", function(){
  console.log('Express server listening on port ' + app.get('port'));
});</pre>

(the port is defined in the <code>app.set('port', process.env.PORT || 3000);</code> section.)

Please also update <strong>public/js/client.js</strong>:
<pre>var socket = io.connect("192.168.1.93:3000");</pre>
with the right IP address/hostname.

To install <code>npm install && bower install</code> and to launch run <code>npm start</code>.

### Whisper

To send a 'private' message, use the following format in the chat message input box:
<code>w:USERNAME:MESSAGE</code> (where 'USERNAME' is the exact name of the user who you wish to whisper to (case-sensitive). For your convenience you can use the whipser link next to the person's username on the left hand side.)

New up to date post: http://tamas.io/further-additions-to-the-node-jssocket-io-chat-app/

Previous articles related to this topic:
<ul>
  <li>http://tamas.io/node-jssocket-io-chat-app-with-geolocation-and-user-agent-support/</li>
  <li>http://tamas.io/chat-2-0-supercharged-chat-written-in-node-js-and-socket-io/</li>
  <li>http://tamas.io/simple-chat-application-using-node-js-and-socket-io/</li>
  <li>http://tamas.io/advanced-chat-using-node-js-and-socket-io-episode-1/</li>
</ul>
