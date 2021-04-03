# ctf_tools
An uncurated list and references to popular open source cybersecurity and network analysis tools. I rely heavily on these for teaching or instructing, and  online CTF competitions.

# Popular Crytography Web Applications
These sites are helpful in encoding and decoding various ciphers. Boxentriq is pretty good at analyzing ciphers if you're not quite sure what it is.
* https://gchq.github.io/CyberChef/
* http://rumkin.com/tools/cipher/
* https://www.boxentriq.com/code-breaking/cipher-identifier
* https://www.dcode.fr/
* https://morsecode.world/international/decoder/audio-decoder-adaptive.html
* https://github.com/Ciphey/Ciphey

# Log Analysis
Analyzing logs can be a very tedious task. Especially, when you you're dealing with thousands of events in a single log. The following is a compilation of useful Linux command line tools that can help you parse out exactly what you're looking for.

The idea is to first review the format of the log so you understand the various fields in each line. Most logs can be unique and custom to an application. For example, a Web Server log will most likely look different than a DNS log. So, pay attention to the delimeter that seperates each field. Sometimes, a space or tab can be the delimeter, but will not necessarily seperate each field perfectly. These utilities can be super helpful, but its always best to try a different combination of the commands to verify your output.

Let's take a web server log. We will use the popular Apache web server for the following examples. A typical log entry looks like the following:
```shell
127.0.0.1 - frank [10/Oct/2000:13:55:36 -0700] "GET /apache_pb.gif HTTP/1.0" 200 2326 "http://www.example.com/start.html" "Mozilla/4.08 [en] (Win98; I ;Nav)"
```

*    
