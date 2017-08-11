# flatrate-sniffer
analyses your internet package consumption, gives you feedback ... 

"# this takes the output of ifconfig and removes everything but the value in question: 

ifconfig |  grep RX | tail -2 | head -1 | sed  s/RX\ packets\ [[:digit:]]\\+\ \\+bytes\ \\+// | sed s/\([[:digit:]]\\+[[:punct:]][[:digit:]]\ MiB\)//

For more details, see the Wiki.

NB. There are two instances in this script that go *double backslash plus* following the [[:digit]] which is supposed to tell sed to use the [[:digit]] command until all numbers before the trailing blank space have been deleted; but that code is only visibe when editing this file. When committed, the double backslash changes to a single backslash! 
