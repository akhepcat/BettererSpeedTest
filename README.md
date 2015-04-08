# BettererSpeedTest

local hacked up version of betterspeedtest.sh, originally coded by Rich Brown.

This version allows for independant up/down testing, and minimal output,
suitable for scripting and import directly into things like RRD databases.

Assuming you have your own netperf server running, test your download-only and get the results in kb/s

    $ BettererSpeedTest -H mynetperf.localdomain -t 30 -n 20 -b -D -q -k | awk '{print $2}'
    15160099


--

Usage: sh BettererSpeedTest [-4 -6] [-qvbkUDHPtpn]

-q|--quiet
-v|--verbose
-b|--bandwidth(-only)
-U|--upload(-only)
-D|--download(-only)
-k|--kilobits                        default: megabits/s
-H|--host netperf-server             default: netperf.bufferbloat.net
-P|--port server-port                default: 12865
-t|--time duration                   default: 30
-p|--ping host-to-ping               default: www.google.com
-n|--number  simultaneous-sessions   default: 20
