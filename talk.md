!SLIDE

<div style="text-align: center;">
	<img src="images/nerdery.png" alt="The Nerdery"/>
</div>

!SLIDE

# Node.js for Nerds
## Stuff that matters

!SLIDE

# Cam Pedersen
## "new guy"

!SLIDE

# Node.js is...

!SLIDE

# Server-side javascript
## Runs on Google's V8 (what makes Chrome fast)

!SLIDE

# Open source

!SLIDE

# Flexible

!SLIDE

# Natively event-based

!SLIDE

# Fast

!SLIDE

# FUN

!SLIDE

# How get?

!SLIDE

# Preflight
## python (you probably have it)
## libssl-dev (if you want to use SSL certificates)

!SLIDE

# The right way

@@@ bash
git clone https://github.com/joyent/node.git
cd node
export JOBS=2 # optional, sets number of parallel commands.
mkdir ~/local
./configure --prefix=$HOME/local/node
make
make install
export PATH=$HOME/local/node/bin:$PATH
@@@

!SLIDE

# The easy way

@@@ bash
wget http://nodejs.org/dist/node-v0.4.7.tar.gz
tar -xzf node-v0.4.7.tar.gz
cd node-v0.4.7
./configure && make && make install
@@@

!SLIDE

# Y U NO SHOW ME CODE?
<img src="images/yuno.jpg" />

!SLIDE

# Count to 20
## count.js

@@@ js

for (var i = 1; i <= 20; i++) {
  console.log(i);
}

@@@

!SLIDE

# In your terminal...

@@@ bash

% node count.js
1
2
3
...

@@@

!SLIDE

# console.log() === var_dump()

!SLIDE

# Count to 20
## count2.js

@@@ js

var c = [];

for (var i = 1; i <= 20; i++) {
  c.push(i);
}

console.log(c);

@@@

!SLIDE

# In your terminal...

@@@ bash

% node count2.js
[1, 2, 3, ...]

@@@

!SLIDE

# A basic web server
## example.js

@@@ js

var http = require('http');

http.createServer(function (req, res) {
  res.writeHead(200, {'Content-Type': 'text/plain'});
  res.end('Hello World\n');
}).listen(1337, "127.0.0.1");

console.log('Server running at http://127.0.0.1:1337/');

@@@

!SLIDE

# In your terminal...

@@@ bash

% node example.js
Server running at http://127.0.0.1:1337/

@@@

!SLIDE
!SLIDE
!SLIDE

# Questions?

[nerdery]: images/nerdery.png
