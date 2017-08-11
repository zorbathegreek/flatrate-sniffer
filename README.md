# flatrate-sniffer
analyses your internet package consumption, gives you feedback ... 

"# this takes the output of ifconfig and removes everything but the value in question: 

ifconfig |  grep RX | tail -2 | head -1 | sed  s/RX\ packets\ [[:digit:]]\\+\ \\+bytes\ \\+// | sed s/\([[:digit:]]\\+[[:punct:]][[:digit:]]\ MiB\)//

For more details, see the Wiki.
