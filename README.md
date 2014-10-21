dockertest
==========
Use docker for testing purpose

commands to start cluster:

docker run --name licensemaster -v /home/docker/license:/license -e LICENSE_FILE=/license/50TB-1.lic -dPt coreqa/splunk lm
docker run --name master -dPt coreqa/splunk master
docker run -dPt --link licensemaster:lm --link master:master coreqa/splunk indexer
docker run -dPt --link licensemaster:lm --link master:master coreqa/splunk indexer
docker run -dPt --link licensemaster:lm --link master:master coreqa/splunk indexer

docker run -dPt --link licensemaster:lm --link master:master coreqa/splunk sh




