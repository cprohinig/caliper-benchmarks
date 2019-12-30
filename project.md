## Prerequisites:

node-gyp, python2, make, g++ and git  
Node.js v8.X LTS or v10.X LTS  
Docker and Docker Compose  

## Install:

npm init -y  
npm install --only=prod @hyperledger/caliper-cli  
npx caliper bind --caliper-bind-sut fabric --caliper-bind-sdk 1.4.1  

## Run benchmark:

npx caliper benchmark run --caliper-benchconfig benchmarks/samples/fabric/marbles/config.yaml --caliper-networkconfig networks/fabric/fabric-v1.4.1/2org1peergoleveldb/fabric-go.yaml --caliper-workspace <path_to_caliper_benchmarks_root_directory>  
  
This will generate a report.html in the specified directory.  
