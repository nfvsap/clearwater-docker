
# Clearwater Docker

1) `git clone https://github.com/nfvsap/clearwater-docker.git`

2) `cd clearwater-docker`

3) `sudo docker build -t clearwater/base base`

4) add your global ip in .env file

5) `sudo docker-compose up -d`

6) exec in cassandra container and bulk create 5000 users
`sudo docker exec -it clearwater-docker_cassandra_1 bash`
`/usr/share/clearwater/crest-prov/src/metaswitch/crest/tools/stress_provision.sh 5000`
wait until Created 5000 users is printed in the console. If this is not printed execute the command again

7) exec in stress-node container and run the stress tests
`sudo docker exec -it clearwater-docker_stress-node_1 bash`
`/usr/share/clearwater/bin/run_stress  example.com 1000 1`
