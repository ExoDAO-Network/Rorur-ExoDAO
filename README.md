Version 2 of the crawler for the Decentralized Search project http://www.searchdao.net (a collaboration between Rorur and ExoDAO). Extremely high performance it runs on distributed clusters. With roughly 1000 machines (AWS EC2 T3) it can crawl much of the indexable Internet in roughly 10 days. It is limited to the "classical Web", does not render and does not support pages driven by dynamic microservices (such as Web 2.0) given their personalized variability.


Build each of the top level files and run them as systemd daemons ( see example.service file). 

Create file /etc/dse/dse.conf with the following information:

directory where data structures will be located

available disk space in GB ( at the moment, we do only namespace crawl so this number must be amortized: multiply your actual disk space by 10^4)

cpu usage ( target cpu usage for single processor)

bandwidth in MB/s ( target BW usage)

