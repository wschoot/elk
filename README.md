es01     | bootstrap check failure [1] of [1]: max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]


sudo sysctl -w vm.max_map_count=262144


h1. json krijgen
root@9f1546365cdb:~# shodan host 94.142.245.155 -O tosca
root@9f1546365cdb:~# ls -la tosca.json.gz
-rw-r--r-- 1 root root 16176 Aug  9 21:05 tosca.json.gz

h1. index maken


root@9f1546365cdb:~# curl -XPUT http://elasticsearch:9200/shodan
{"acknowledged":true,"shards_acknowledged":true,"index":"shodan"}root@9f1546365cdb:~#

h1. .env file

put your shodan API key in .env file
