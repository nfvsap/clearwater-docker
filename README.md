
# Clearwater Docker

1) `git clone https://github.com/nfvsap/clearwater-docker.git`

2) `cd clearwater-docker`

3) `sudo docker build -t clearwater/base base`

4) add your global ip in .env file

5) `sudo docker-compose up -d`

6) exec in cassandra container and 
`/usr/share/clearwater/crest-prov/src/metaswitch/crest/to/stress_provision.sh 5000`

7) exec in stress-node container and
`/usr/share/clearwater/bin/run_stress  example.com 1000 1`
