# flatrate-sniffer
analyses your internet package consumption, gives you feedback ... 

"# this takes the output of ifconfig and removes everything but the value in question     
ifconfig |  grep RX | tail -2 | head -1 | sed 's/RX\ packets\ [[:digit:]]\+\ \ bytes//' | sed s/[[:punct:]][[:digit:]]\\+[[:punct:]][[:digit:]]\ MiB[[:punct:]]//

"# We can now compare that number to the package we bought from our favourite ISP, like 1.2 Gb, and set off some kind of visual or audio feedback when we are approaching the end of our capacity. 
"# 
