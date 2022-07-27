*SETUP BACKEND*

A. change values in .env

1. PRIVATE_KEY: Private key of the that wallet through which new token will be    sent to the user after swap.
'Most Important:'
- Whitelist this wallet (Exclude this wallet from all charges, and rewards)
- Keep Sufficient new tokens for swap in this wallet
- Keep sufficient BNB for gas fee as well in this wallet(e.g If target swap user is 1000 than as per current gas price i.e 0.0013 keep 0.0013 x 1000=1.3 BNB in this wallet)
- never commit this to github that will expose private key to world and you can loose all funds.

2. FMC_NEW_CONTRACT- Contract address of the new FMC contract i.e 0xd1baaed91361cea01a2d9be0ca8988756163971a
3. FMC_NEW_CONTRACT_ABI - you can find ABI JSON from https://bscscan.com/address/0xd1baaed91361cea01a2d9be0ca8988756163971a#code
4. RPC_URL - Network RPC URL for BNB main net it is https://bsc-dataseed1.binance.org/

*Installation Steps EC2 instance:*
1. Log in to the server 
2. go to the folder BACKEND
3. run npm install
3. run 'node index &'
4. to change port go to index.js line no. 5


*EXTRA INFORMATION*
1. Logs are recorded in transaction.json file
2. You can change res.setHeader('Access-Control-Allow-Origin','*'); at line#18 for safety

