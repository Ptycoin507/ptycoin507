# ptycoin
Ptycoin Cryptomoneda de Panamá

Use the following instructions to mine a block.

Open your wallet, and make sure your wallet is connected with a node. 
Your wallet is connected when you see the icon Wallet connections Scrypt and SHA256 in the lower right corner of your wallet.

The message “Syncing Headers (0,0%)” will disappear once you mine your first block.

Close your wallet and create the file ptycoin507.conf in the folder “%APPDATA%\ptycoin507\”.

Paste the following text into ptycoin507.conf and save the file.

rpcuser=rpc_ptycoin507
rpcpassword=eeda12757789dc4edd93efed7
rpcallowip=127.0.0.1
rpcport=11225
listen=1
server=1
addnode=ptycoin507node.ddns.net
addnode=ptycoin507usa.ddns.net
addnode=ptycoin507.ddns.net

Open your wallet.

Create a .bat file named mine.bat in the same folder where you extracted ptycoin507-cli.exe and paste the following text into mine.bat.

@echo off
set SCRIPT_PATH=%cd%
cd %SCRIPT_PATH%
echo Press [CTRL+C] to stop mining.
:begin
 ptycoin507-cli.exe generate 1
goto begin 

Save the file.

Execute mine.bat to start mining your first block.

It will take about +/- 30 minutes to mine your first block, depending on your computer hardware.
