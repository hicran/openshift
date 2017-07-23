Elasticsearch Docker Image
======================

This repository contains Dockerfiles to run Elasticsearch under OpenShift v3 as a docker image.
Current Elasticsearch version is 5.5.0.

Running Locally
---------------

To build and run locally, execute:

    git clone https://github.com/hicran/openshift.git
    docker build -t elasticsearch:5.5 elasticsearch/5.5/
    docker run -d elasticsearch:5.5

