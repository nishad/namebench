Are you a power-user with 5 minutes to spare? Do you want a faster internet experience?

Try out namebench. It hunts down the fastest <a href='http://en.wikipedia.org/wiki/Domain_Name_System'>DNS servers</a> available for your computer to use. namebench runs a fair and thorough benchmark using your web browser history, tcpdump output, or standardized datasets in order to provide an individualized recommendation. namebench is completely free and does not modify your system in any way. This project began as a 20% project at Google.

namebench runs on Mac OS X, Windows, and UNIX, and is available with a graphical user interface as well as a command-line interface.<br /><img src='http://namebench.googlecode.com/files/screenshot-1.3.png'><br />
namebench was written using open-source tools and libraries such as <a href='http://www.python.org/'>Python</a>, <a href='http://wiki.python.org/moin/TkInter'>Tkinter</a>, <a href='http://pyobjc.sourceforge.net/'>PyObjC</a>, <a href='http://www.dnspython.org/'>dnspython</a>, <a href='http://jinja.pocoo.org/2/'>jinja2</a> and <a href='http://graphy.googlecode.com/'>graphy</a>.<br>
<br>
<h1>Screenshots</h1>

Here is what the nameserver overview looks like:<br>
<br>
<img src='http://namebench.googlecode.com/files/screenshot-1.3-table.jpg'>

Here are what some of the graphs produced look like:<br>
<br>
<img src='http://namebench.googlecode.com/files/screenshot-1.3-graphs.jpg'>

<h2>Command-line version</h2>

If you are running the command-line version, you get something that looks like this:<br>
<br>
<br>
<pre><code>Final list of nameservers considered:<br>
------------------------------------------------------------------------------<br>
130.85.1.5      UMBC 5 US          56  ms | <br>
208.67.222.220  OpenDNS-3          56  ms | www.google.com is hijacked: google.navigation.opendns.com<br>
209.244.0.4     Level3-R2          62  ms | <br>
216.146.35.35   DynGuide           63  ms | NXDOMAIN Hijacking<br>
204.9.56.9      BroadAspect US     63  ms | <br>
8.8.4.4         Google Public DNS- 64  ms | Replica of Google Public DNS [8.8.8.8]<br>
208.67.220.220  OpenDNS            65  ms | www.google.com is hijacked: google.navigation.opendns.com<br>
156.154.70.1    UltraDNS           67  ms | NXDOMAIN Hijacking<br>
127.0.0.1       Localhost IPv4     68  ms | NXDOMAIN Hijacking (www)<br>
209.18.47.61    RoadRunner NC US   68  ms | Replica of RoadRunner NC-2 US [209.18.47.62], NXDOMAIN Hijacking (www)<br>
156.154.71.22   Comodo Secure DNS- 80  ms | NXDOMAIN Hijacking<br>
209.18.47.62    RoadRunner NC-2 US 104 ms | (excluded: Slower replica of RoadRunner NC US [209.18.47.61])<br>
<br>
- Sending 250 queries to 11 servers...<br>
<br>
Mean response (in milliseconds):<br>
--------------------------------<br>
Google Public DN ################# 64.85<br>
Comodo Secure DN ################### 72.84<br>
RoadRunner NC US ####################### 91.19<br>
UltraDNS         ####################### 91.61<br>
Localhost IPv4   ########################### 108.66<br>
OpenDNS          ############################ 110.69<br>
OpenDNS-3        ###################################### 149.85<br>
DynGuide         ####################################### 156.60<br>
Level3-R2        ########################################### 169.81<br>
UMBC 5 US        ########################################### 172.63<br>
BroadAspect US   ##################################################### 214.19<br>
<br>
Response Distribution Chart URL (200ms):<br>
----------------------------------------<br>
http://chart.apis.google.com/chart?cht=lxy&amp;chs=720x415&amp;chxt=x,y&amp;chg=10,20&amp;chxr=0,0,200|1,0,100&amp;chd=t:0,8,8,9,10,1...<br>
<br>
Response Distribution Chart URL (Full):<br>
---------------------------------------<br>
http://chart.apis.google.com/chart?cht=lxy&amp;chs=720x415&amp;chxt=x,y&amp;chg=10,20&amp;chxr=0,0,3500|1,0,100&amp;chd=t:0,0,0,1,1,1...<br>
<br>
Recommended configuration (fastest + nearest):<br>
----------------------------------------------<br>
nameserver 8.8.4.4         # Google Public DNS-2  <br>
nameserver 127.0.0.1       # Localhost IPv4  <br>
nameserver 209.18.47.62    # RoadRunner NC-2 US  <br>
<br>
<br>
</code></pre>