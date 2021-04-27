# Unit 21: You sure can attract a crowd!

Your company has decided to crowdsale their PupperCoin token in order to help fund the network development.
This network will be used to track the dog breeding activity across the globe in a decentralized way, and allow humans to track the genetic trail of their pets. You have already worked with the necessary legal bodies and have the green light on creating a crowdsale open to the public. However, you are required to enable refunds if the crowdsale is successful and the goal is met, and you are only allowed to raise a maximum of 300 Ether. The crowdsale will run for 24 weeks.

This crowdsale contract will manage the entire process, allowing users to send ETH and get back PUP (PupperCoin).
This contract will mint the tokens automatically and distribute them to buyers in one transaction.

#### PupperCoinCrowdsale

- `RefundablePostDeliveryCrowdsale` inherits the `RefundableCrowdsale` contract, which requires a `goal` parameter.
- Call the `RefundableCrowdsale` constructor from the `PupperCoinCrowdsale` constructor as well as the others.
- `RefundablePostDeliveryCrowdsale` does not have its own constructor and thus use the `RefundableCrowdsale` constructor that it inherits.
- Pass the `open` and `close` times by using `now` and `now + 24 weeks` to set the times properly from `PupperCoinCrowdsaleDeployer` contract.

#### PupperCoinCrowdsaleDeployer



### Deploying the Crowdsale

Deploy the crowdsale to the Kovan or Ropsten testnet, and store the deployed address for later. Switch MetaMask to your desired network, and use the `Deploy` tab in Remix to deploy your contracts. Take note of the total gas cost, and compare it to how costly it would be in reality. Since you are deploying to a network that you don't have control over, faucets will not likely give out 300 test Ether. You can simply reduce the goal when deploying to a testnet to an amount much smaller, like 10,000 wei.
