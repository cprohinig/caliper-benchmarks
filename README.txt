# Caliper Benchmarks Project

Christof Karisch, Milan Davidovic, Christian Prohinig

## Prerequisites:

The following have to be installed for the next steps to work:  
  
node-gyp, python2, make, g++ and git  
Node.js v8.X LTS or v10.X LTS  
Docker and Docker Compose  

## Install:
Init npm and install caliper locally in caliper-benchmarks (root of project) directory:  

npm init -y  
npm install --only=prod @hyperledger/caliper-cli  
npx caliper bind --caliper-bind-sut fabric --caliper-bind-sdk 1.4.1  

## Run benchmark:
Run the benchmark inside the caliper-benchmarks (root of project) directory:  

npx caliper benchmark run --caliper-benchconfig benchmarks/config.yaml --caliper-networkconfig networks/fabric/fabric-v1.4.1/2org1peergoleveldb/fabric-go.yaml --caliper-workspace "$(pwd)"  

This will generate a report.html directly in caliper-benchmarks (root of project), which can be viewed in the browser.  
We added report.pdf containing a description of the results.    
