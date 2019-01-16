# hyperledger_smart_contract_user_sample

I am assuming that you are having a runnning hyperledger network

## To Install chaincode run ##
`peer chaincode install -n pankajusercc -v 0 -p "Directory where you cloned dummyuser.go"`

## To Instansiate chaincode ##
`peer chaincode upgrade -n pankajusercc -v 0 -c '{"Args":[]}' -o 127.0.0.1:7050 -C "your channel name here"`


## To Add a user ##

`peer chaincode invoke -n mycc -c '{"Args":["addUser","1234","{\"first_name\":\"pankaj\",\"last_name\":\"cheema\",\"roll\":23 } "]}' -o 127.0.0.1:7050 -C "your channel name here"`

## To Get the user ##

`peer chaincode query -n mycc -c '{"Args":["getUser","1234"]}'  -C ch1`