### OpenShift Blockhain Consortium starter 

# A starting point for custom Parity Ethereum networks via Openshift 

Template contains 1 Validator (authority) ethereum node, 3 load balanced, fatDB enabled, Secondary ethereum nodes, 1 Block explorer

The persistent (1gb default) Validator node will automatically start to produce blocks.

Ephemeral Secondary nodes should connect to Validator node by themselves, if required - restart the nodes after some time.

Block explorer requests are load-balanced across the three secondary nodes.

![alt text][r1]
![alt text][r2]
![alt text][r3]


[r1]: images/consortium-starter-1.png ""
[r2]: images/consortium-starter-2.png ""
[r3]: images/consortium-starter-3.png ""
