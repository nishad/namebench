These docs cover use of the UI, for command-line specific help, see UsingNameBenchCommandLine

# Using namebench #

When you start namebench on Mac OS X, Windows, or Linux with the required libraries (python-tk), you will be greeted with a basic interface:

<img src='http://namebench.googlecode.com/files/screenshot-1.3.png'>

The defaults should do the right thing for nearly everyone, so most people can safely click "Start Benchmark". Once the benchmark runs, a web browser should pop-up with a detailed analysis.<br>
<br>
<h2>Options</h2>

<h3>Nameservers</h3>

This is a list of any specific nameservers that you would like to make sure are included in the benchmark. By default, this includes all of the nameservers that your system is currently using. You can specify multiple nameservers by using a comma or space in between them.<br>
<br>
<h3>Include global DNS providers</h3>

Selecting this will include well-known DNS providers with global coverage into your benchmark. At the time of this writing, this includes OpenDNS and UltraDNS. Power-users can alter this list by editing namebench.cfg.<br>
<br>
<h3>Include best available regional DNS services</h3>

Selecting this will include the fastest regional DNS servers in your test. This works by quickly testing the health of over 1,000 DNS servers around the world, and selecting only the fastest servers that provide correct responses.<br>
<br>
NOTE: The namebench UI restricts you to testing a total of 10 nameservers at a time. If your system has a primary and secondary DNS server, and 4 global DNS servers to test, only the best 4 regional DNS servers will be used in the benchmark.<br>
<br>
<h3>Include Censorship Checks</h3>

namebench includes a list of hostnames for popularly censored website. With this option enabled, it will request these hosts and check to make sure the results are as expected.<br>
<br>
<br>
<h3>Upload and Share</h3>

namebench can now upload and published anonymized version of your results to the <a href='http://namebench.appspot.com/'>namebench reports site</a>. This feature is not only useful if you would like to show someone else your results, but it helps ISP's who run DNS servers collect information on their own performance. Feedback collected is also used to improve namebench.<br>
<br>
To see a technical description of what data is uploaded, see <a href='http://code.google.com/p/namebench/source/browse/trunk/JSON.txt'>JSON.txt</a>.<br>
<br>
<h3>Your location</h3>

At the moment, this field is unused.<br>
<br>
<br>
<h3>Query Data Source</h3>

namebench works by requesting website addresses from each DNS server. This dialog allows you to select where this list of host names are generated from. The most accurate data source is your browser history, though for smaller histories, the benchmark may bias toward your currently configured primary DNS server. This list contains each browser that namebench was able to find a history for, along with how many records it found in the history file (in parenthesis).<br>
<br>
This list also contains "Alexa Top Global Domains (10000)". This data source contains a list of the domains for the  top 10,000 most popular websites on the Internet. While this data set is useful, it does not necessarily reflect your DNS use. For example, this list contains many domains in China that someone who lives in Finland is unlikely to query for.<br>
<br>
<h3>Health Check Performance</h3>

This option tells namebench how many DNS servers it can access at the same time for health checking. Normally, you want the fast option (40 servers). If you have problems with your internet connection however, you may want to select the slow option (10 servers).<br>
<br>
<h3>Number of queries</h3>

This option selects how many requests should be tested for each DNS server. The more tests, the more the results should reflect real-world usage. By default we send 250 requests for each name server.<br>
<br>
<h2>Output</h2>

Once the run completes successfully, your default web browser should pop-up with a report. It should be self-explanatory:<br>
<br>
<img src='http://namebench.googlecode.com/files/screenshot-1.3-table.jpg'>