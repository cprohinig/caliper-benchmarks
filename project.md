## Prerequisites:

node-gyp, python2, make, g++ and git  
Node.js v8.X LTS or v10.X LTS  
Docker and Docker Compose  

## Install:
Init npm and install caliper locally in caliper-benchmarks directory:  

npm init -y  
npm install --only=prod @hyperledger/caliper-cli  
npx caliper bind --caliper-bind-sut fabric --caliper-bind-sdk 1.4.1  

## Run benchmark:
Run the benchmark inside the caliper-benchmarks directory:  

npx caliper benchmark run --caliper-benchconfig benchmarks/samples/fabric/marbles/config.yaml --caliper-networkconfig networks/fabric/fabric-v1.4.1/2org1peergoleveldb/fabric-go.yaml --caliper-workspace "$(pwd)" 
  
This will generate a report.html directly in caliper-benchmarks root.  
