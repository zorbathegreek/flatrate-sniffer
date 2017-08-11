# flatrate-sniffer
analyses your internet package consumption, gives you feedback ... 

"# this takes the output of ifconfig and removes everything but the value in question: 

ifconfig |  grep RX | tail -2 | head -1 | sed 's/RX\ packets\ [[:digit:]]\+\ \ bytes//' | sed s/[[:punct:]][[:digit:]]\\+[[:punct:]][[:digit:]]\ MiB[[:punct:]]//

For more details, see the Wiki.
