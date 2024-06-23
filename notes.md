deployed contract address: credible_squaring_avs_deployment_output.json

One time install
```
curl -L https://foundry.paradigm.xyz | bash
foundryup
go install github.com/maoueh/zap-pretty@latest
```

If you want to build contracts
```
make build-contracts
```

Run phi docker.

Run commands in different terminals:
```
make start-anvil-chain-with-el-and-avs-deployed
make start-aggregator
make start-operator
```

Send user request as a string:
```
curl --location 'http://127.0.0.1:8091/user-request' \
--header 'Content-Type: application/json' \
--data '{
    "Id": "1234",
    "userRequest": "how r u"
}'
```

Get response:
```
curl --location 'http://127.0.0.1:8094/user-response?Id=1234'
```
