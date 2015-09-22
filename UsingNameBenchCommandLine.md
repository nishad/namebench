# namebench command-line usage #

First, download the namebench source code file and extract it. You will also need <a href='http://www.python.org/'>Python</a> 2.5 - 2.7 installed. Mac OS X and most UNIX distributions come with this already. Assuming all of this, it's normally just as easy as typing:

```
 ./namebench.py 
```

If namebench launches a graphical window (because you have Tk), you can use the -x option to force it to command-line mode.

namebench will test the nameservers your machine is currently using, plus
the popular global DNS services, and the best 4-6 additional name servers
that it can find for you. It will output some text-graphs and URL's for more
a more detailed performance analysis of each nameserver.

If you want to specify an additional set of name services, simply add the IP
to the command-line, or edit namebench.cfg:

```
  ./namebench.py 10.0.0.1 192.168.0.1
```

# Options #

```
Usage: namebench.py [options]

Options:
  -h, --help            show this help message and exit
  -r RUN_COUNT, --runs=RUN_COUNT
                        Number of test runs to perform on each nameserver.
  -z CONFIG, --config=CONFIG
                        Config file to use.
  -o OUTPUT_FILE, --output=OUTPUT_FILE
                        Filename to write output to
  -t TEMPLATE, --template=TEMPLATE
                        Template to use for output generation (ascii, html,
                        resolv.conf)
  -c CSV_FILE, --csv_output=CSV_FILE
                        Filename to write query details to (CSV)
  -j HEALTH_THREAD_COUNT, --health_threads=HEALTH_THREAD_COUNT
                        # of health check threads to use
  -J BENCHMARK_THREAD_COUNT, --benchmark_threads=BENCHMARK_THREAD_COUNT
                        # of benchmark threads to use
  -P PING_TIMEOUT, --ping_timeout=PING_TIMEOUT
                        # of seconds ping requests timeout in.
  -y TIMEOUT, --timeout=TIMEOUT
                        # of seconds general requests timeout in.
  -Y HEALTH_TIMEOUT, --health_timeout=HEALTH_TIMEOUT
                        health check timeout (in seconds)
  -i INPUT_SOURCE, --input=INPUT_SOURCE
                        Import hostnames from an filename or application
                        (alexa, cachehit, cachemiss, cachemix, camino, chrome,
                        chromium, epiphany, firefox, flock, galeon, icab,
                        internet_explorer, konqueror, midori, omniweb, opera,
                        safari, seamonkey, squid, sunrise)
  -I, --invalidate_cache
                        Force health cache to be invalidated
  -q QUERY_COUNT, --query_count=QUERY_COUNT
                        Number of queries per run.
  -m SELECT_MODE, --select_mode=SELECT_MODE
                        Selection algorithm to use (weighted, random, chunk)
  -s NUM_SERVERS, --num_servers=NUM_SERVERS
                        Number of nameservers to include in test
  -S, --system_only     Only test current system nameservers.
  -w, --open_webbrowser
                        Opens the final report in your browser
  -u, --upload_results  Upload anonymized results to SITE_URL (False)
  -U SITE_URL, --site_url=SITE_URL
                        URL to upload results to
                        (http://namebench.appspot.com/)
  -H, --hide_results    Upload results, but keep them hidden from indexes.
  -x, --no_gui          Disable GUI
  -C, --enable-censorship-checks
                        Enable censorship checks
  -6, --ipv6_only       Only include IPv6 name servers
  -O, --only            Only test nameservers passed as arguments
```

# Configuration Files #

Most everything about namebench can be tweaked: See the config/ subdirectory for more information.