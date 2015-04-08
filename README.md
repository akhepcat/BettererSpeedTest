# BettererSpeedTest

local hacked up version of betterspeedtest.sh, originally coded by Rich Brown.

This version allows for independant up/down testing, and minimal output,
suitable for scripting and import directly into things like RRD databases.

Assuming you have your own netperf server running:

    BettererSpeedTest -H mynetperf.localdomain -t 30 -n 20 -b -D -q -k | awk '{print $2}'
    15160099

