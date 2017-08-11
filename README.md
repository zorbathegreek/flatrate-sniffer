# flatrate-sniffer
analyses your internet package consumption, gives you feedback ... 

"# this takes the output of ifconfig and removes everything but the value in question: 

ifconfig |  grep RX | tail -2 | head -1 | sed 's/RX\ packets\ [[:digit:]]\+\ \ bytes//' | sed s/[[:punct:]][[:digit:]]\\+[[:punct:]][[:digit:]]\ MiB[[:punct:]]//

We can now compare that number to the package we bought from our favourite ISP, like 1.2 Gb, and set off some kind of visual or audio feedback when we are approaching the end of our capacity, be it datawise or timewise. We do not want to run out of data prematurely, so we need to get a warning if we are running down the remaining data credit; we also do not want to Not use data that we paid for, so we need to get a warning if the time is running out "soon". We could update our system, initiate or increase the speed of a running download, ...

We have to keep in mind that ifconfig resets at boot time. So we need to make our numbers survive a reboot and add the script output to what we had previously. 

We also have to make our script reset to zero if we reload a daily/weekly/monhly flatrate. 

