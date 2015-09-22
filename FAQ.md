

# What does namebench actually do? #

namebench looks for the fastest DNS (<a href='http://en.wikipedia.org/wiki/Domain_Name_System'>Domain Name System</a>) servers accessible to your computer. You can think of a DNS server as a phone book: When you want to dial a company on the phone, you may have to flip through a phone book by name to find their phone number. On the internet, when you want to visit "www.google.com", a DNS server needs to looks up the correct <a href='http://en.wikipedia.org/wiki/IP_address'>IP Address</a> for you.

Over the course of loading a single web page, your computer may need to look up a dozen of these addresses. While your internet provider usually automatically assigns you one of their servers to handle looking up these addresses, there may be others that are significantly faster.

namebench finds them.

# Will namebench make surfing the web faster? #

Yes.

# Will namebench make large downloads faster? #

Probably not.

While namebench may significantly increase the speed of every day websurfing, it will not increase the speed of large file downloads such as watching movies online. This is because your computer only has to perform DNS lookups to start the download of the movie. Once the download initiates successfully, your download performance is at the mercy of your internet provider.

# Can I run namebench while downloading large files? #

namebench assumes your connection has a low amount of traffic while it is running. If this is not the case, the results will be less useful.



# Running namebench #

## namebench fails to start on Windows 2000, XP, or Vista ##

If you get one of the following errors, your system is missing the Microsoft 2008 Visual C++ libraries:

_namebench could not  be executed._

_This application has failed to start because the application configuration
is incorrect. Reinstalling the application may fix this problem._

To fix this, download the package from Microsoft: <a href='http://www.microsoft.com/downloads/details.aspx?familyid=A5C84275-3B97-4AB7-A40D-3802B2AF5FC2&displaylang=en'>Microsoft Visual C++ 2008 SP1 Redistributable Package (x86)</a>.

## namebench fails to start on Mac OS X 10.4 ##

The default Mac user interface requires Mac OS X 10.5 or higher. As a workaround, you can download the namebench source code, open Terminal.app, and type the following to launch the Tk GUI:

```
I_LOVE_TK=1 ./namebench.py
```

## What packages do I need for the UI in UNIX? ##

Without the proper libraries installed, namebench will fall back to the command-line version. If you would like a UI:

  * Debian/Ubuntu: sudo apt-get install python-tk
  * Fedora: yum install tkinter
  * FreeBSD: sudo pkg\_add -r py-tkinter

# Interacting with namebench #

# Using the Results #

## How do you use the DNS servers recommended? ##

See http://code.google.com/speed/public-dns/docs/using.html

Please note: If this machine is part of a larger internal network, use of an external DNS server may result in not being able to access other machines within the network. This should not affect home use, however.

## Why do I get different results each time I run namebench. ##

The first run is the one that is most likely to be accurate. The more times to run namebench, the more likely you are to be repeating the same queries over and over again. This will skew your results toward the closest nameserver to you, rather than the one most likely to have your requests cached during normal operations.

One work-around to avoid this is to switch between the Alexa dataset and your favorite browser as a history source. As the Alexa dataset is global in scope, it will tend to skew toward nameservers that cache queries from around the world, however.

## I run my own nameserver at home, why is it slower? ##

A nameserver with only a few users is less likely to have as many hostnames in it's cache as ones with a larger pool of users. While the latency for cached results will be fastest from a DNS server on the same network as the client, this advantage is easily offset if the majority of requests are not able to be fulfilled from cache.

## What does "NXDOMAIN hijacking" mean? ##

It means that the DNS server falsifies the result when a non-existent host is requested. This is usually used so that the DNS provider can place advertising when you make a typo when typing in a URL.

## What does "Incorrect result for..." mean? ##

This means that the DNS server may be falsifying the result for a well known service, and redirecting you to another website. This is usually a very bad thing. This alert may also result in false positives when a website changes to a new network or CNAME.

# Other Questions #

## What do you do with the browser history? ##

namebench looks up what hostnames your web browser has accessed, and replays the requests for a random selection of hosts to the 11 best DNS servers. Alternatively, you can also use the Alexa Top 10,000 domains as a data source, though the queries will be not be personalized, and the results less accurate as a result.

## Are all of the "regional servers" public? ##

_If I do a test run, and it points me at various regional DNS servers, run
by ISPs or transit providers, are these servers officially "public"?_

No. Many regional nameservers are only available to their direct or indirect customers. The ones that do show up on your list are the ones that do allow recursive lookups to your machine however. Like accessing a web page found on a search engine, it is possible that the DNS server was misconfigured to allow public access, and may disappear at any time.

## I run a public nameserver, how do I get added or removed? ##

<a href='http://code.google.com/p/namebench/issues/entry'>Enter an issue</a> with a list of IP's to include or exclude.

## How do I submit a bug? ##

See <a href='http://code.google.com/p/namebench/issues/list'>our issue tracker</a>

## Where can I discuss namebench? ##

Visit <a href='https://groups.google.com/group/namebench'>namebench on Google Groups</a>