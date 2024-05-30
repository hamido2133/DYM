# DYM
NODE
A registry for RollApps on Froopyland testnet:

This repository is dedicated to the listing process of RollApps on the Portal.

Please follow the instructions for listing a RollApp:

Make sure to have successfully deployed and are running a RollApp instance.

Fund the Faucet and test the IBC connection by submitting an IBC transfer of your RollApp token to the Dymension Hub faucet with the following command:

roller tx fund-faucet
Subsequently, check the balance of the RollApp token on the Dymension Hub faucet which should arrive within 15 minutes:

$balance dym1g8sf7w4cz5gtupa6y62h3q6a4gjv37pgefnpt5 <RollApp-ID>
Fork the RollApp-registry repo into your GitHub account.

Clone it by running the following command:

git clone https://github.com/<your-github-username>/rollapp-registry
CD into the cloned repo:

cd rollapp-registry
Retrieve your generated rollapp id with roller config show and save it as an environment variable:

export ROLLAPP_ID=<RollApp-ID-HERE>
Create the appropraite folders and files:

cd devnet
mkdir -p $ROLLAPP_ID/logos
cd $ROLLAPP_ID && touch $ROLLAPP_ID.json
This should create a folder for your RollApp logo and config information.

Add your RollApp logo to the logos folder. Logo file name: <RollApp-ID>.<format>. This can be SVG, PNG, or JPG format. Please make sure the file doesn't exceed 50KB.

Export the RollApps configuration JSON by running:

roller config export
Copy paste the JSON output to the <RollApp-ID>.json and fill in the following fields:

RPC: "http://<your-ip-or-domain>:<port>" (default port 26657)
REST:  "http://<your-ip-or-domain>:<port>" (default port 1317)
EVM RPC *(ONLY FOR EVM ROLLAPPS): "http://<your-ip-or-domain>:<port>" (default port 8545)
Logo path: "/logos/<RollApp-ID>-logo.svg"
Optinal fields:

chainName: from <RollApp-ID>to your RollApp's name as it will appear on the Portal
description: add "<Your RollApp description>", to be displayed on the portal
website: add "<your-RollApp's-url>", to be displayed on the portal
Add and commit your changes:

git add .
git commit -m "added RollApp"
git push -u origin main
Create a PR to https://github.com/dymensionXYZ/rollapp-registry.

For a demonstration of a step-by-step guide to creating a PR please follow the GitHub documentation or watch this helpful youtube video.

Pair the RollApp on the Discord channel by entering the following command: (In the following command replace <RollApp-ID> with your customized RollApp ID.)

$pair <RollApp-ID>
A community moderator will then begin a conversation with you in Discord. Please follow attentively to get the listing process fulfilled quickly.

If you have any question please feel 
