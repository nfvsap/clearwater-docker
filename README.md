
# Clearwater Docker

1) `git clone https://github.com/nfvsap/clearwater-docker.git`

2) `cd clearwater-docker`

3) add your global ip in .env file

4) `sudo docker-compose up -d`

5) exec in cassandra container and 
`/usr/share/clearwater/crest-prov/src/metaswitch/crest/to/stress_provision.sh 5000`

6) exec in stress-node container and
`/usr/share/clearwater/bin/run_stress  example.com 1000 1`
