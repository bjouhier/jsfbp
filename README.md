jsfbp
=====

Basic FBP implementation written in JavaScript, using Node-Fibers - https://github.com/laverdet/node-fibers .

General
---

Very early feasibility study.

Current test case has 3 processes:
 - `Sender`
 - `Copier`
 - `Recvr`

![JSFBP](https://github.com/jpaulm/jsfbp/blob/master/docs/JSFBP.png "Simple Test Network")

Install & Run
---

Install node-fibers via npm: just do `npm install fibers`.

Create a folder called `jsfbp` in `node/node_modules/fibers`, and download the 5 JavaScript files from the JSFBP `script` directory into `jsfbp`.

This network can now be run by positioning at this directory, and entering `node fbptest.js`.  If tracing is desired, change the value of the `trace` variable at the bottom of fbptest.js to `true`.

Programming issues
---
Objects are `Process` and `Connection`; currently we don't have any Port objects (Connections are attached directly to Process instances) - this may change.

Performance
---

This first test case (Jan. 16, 2015) with 2000 IPs running through three processes takes 200 ms, giving approx. 50 microsecs per send/receive pair.  

