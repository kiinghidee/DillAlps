# DillAlps
Na the system requirement be this
Light Validator: 2 cores 2G Ram SSD: 20GB 8Mb/s Ubuntu LTS 20.04+/MacOS
Full Validator: 4 cores 8G Ram SSD: 256GB 64Mb/s Ubuntu LTS 20.04+/MacOS
Steps to take set up and codes
I still make video for the setup, you fit find am for here. The steps wey I go talk about dey for the video. First, we go start with the code wey the team release for one line.
bash
Copy code
curl -sO https://raw.githubusercontent.com/DillLabs/launch-dill-node/main/dill.sh  && chmod +x dill.sh && ./dill.sh
The first message wey go show go get two options. For here, we go pick number 1 (Launch a new dill node) then press enter make we continue.

For this step, number 1 go generate new validator key (mnemonic), you gatz use program like winscp take back am up well well (go copy the full /root/dill/validator_keys folder, e go get the mnemonic and password wey dem generate). If you wan use the old mnemonic, pick number 2 (I go advice say make you back up the validator_keys folder).

The next step na deposit step. For Discord, you go gatz use faucet for alps channel. If faucet send 3600, na Light Validator you go run, but if dem send 36000, na Full Validator. After you collect faucet, check your address for here: https://alps.dill.xyz/ to see how much you don get.

E go ask you for Withdrawal address, any EVM wallet fit work. Me I use the same wallet wey I take collect faucet.

When "Step 2 Completed" show, press any key and wait till e finish. Then e go show "node running" and go give you the pubkey for your Validator. You gatz write am down well well.

Stake Steps
After the node don sync with the system, follow the steps below to stake. You fit use any of these codes:
bash
Copy code
cd dill
./health_check.sh -v
curl -s localhost:3500/eth/v1/beacon/headers | jq
curl -s localhost:3500/eth/v1/node/syncing
Go https://staking.dill.xyz/en/ and upload the deposit_data-xxxx.json file from the validator_keys folder wey you save.

After you upload am, press next. For the next screen, when you connect Metamask, e go show your wallet balance. The correct amount go show based on the node type. Approve am and press next.

For the next step, press "Send Deposit" and when Metamask warning show, you go see the deposit amount either 3600 or 36000. After you approve am, after some time you go see screen wey be like this below.

Finally, when you search for your validator public key for the dillscan validator page, e go show the info about your validator. After the approval step, in about 1 hour you go fit see am for dillscan. Good luck!
