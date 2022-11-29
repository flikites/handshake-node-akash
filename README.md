# handshake-full-listening-node-akash

This is an SDL file that will deploy a full listening handshake node onto akash.

[Link to Akash SDL File](https://github.com/WireWrex/handshake-node-akash/blob/main/handshake-node-fl.sdl)

Deploy using CloudMOS: https://cloudmos.io/cloud-deploy

Open Cloudmos and click "Deploy" 

Step 0: Choose the "Empty" option and paste the [SDL](https://github.com/WireWrex/handshake-node-akash/blob/main/handshake-node-fl.sdl) file.

Step 1: Create a unique name under```endpoints:``` . You will be changing line 4. Leave the colon.

Step 2: Use the same name to replace line 14. Leave ip: only change the name.

Step 3: Wait until the blockchain has synced (check the "logs" tab to see chain height) then edit the --public-host environment variable to reflect the instances public/static IP address. (Check the "Leases" tab for the IP) Once changed, click "Update Deployment"


More information related to handshake node configuration types: https://hsd-dev.org/guides/config.html

# Full Node that allows inbound connections from other full and light clients like hnsd
<IP address> MUST be your external IP address, publicly accessible by the internet.

hsd \
--bip37=true   \
--listen=true   \
--public-host=<IP address>
--public-port=12038  \
--max-inbound=100	




