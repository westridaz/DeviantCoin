# Deviant Coin
Shell script to install an [Deviant Coin Masternode](http://http://deviantcoin.io/) on a Linux server running Ubuntu 16.04. Use it on your own risk.  

***
## Installation:  

wget -q https://raw.githubusercontent.com/zoldur/DeviantCoin/master/deviant_install.sh  
bash deviant_install.sh
***

## Desktop wallet setup  

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps:  
1. Open the Deviant Coin Desktop Wallet.  
2. Go to RECEIVE and create a New Address: **MN1**  
3. Send **5000** DEV to **MN1**.  
4. Wait for 15 confirmations.  
5. Go to **Help -> "Debug window - Console"**  
6. Type the following command: **masternode outputs**  
7. Go to **Masternodes** tab  
8. Click **Create** and fill the details:  
* Alias: **MN1**  
* Address: **VPS_IP:PORT**  
* Privkey: **Masternode Private Key**  
* TxHash: **First value from Step 6**  
* Output index:  **Second value from Step 6**  
* Reward address: leave blank  
* Reward %: leave blank  
9. Click **OK** to add the masternode  
10. Click **Start All**  

***

## Multiple MN on one VPS:

Whilst not recommended, it is possible to run multiple **Deviant** Master Nodes on the same VPS. Each MN will run under a different user you will choose during installation.  

***


## Usage:  

For security reasons **Deviant** is installed under **deviant** user, hence you need to **su - deviant** before checking:    

```
DEVIANT_USER=deviant #replace deviant with the MN username you want to check

su - $DEVIANT_USER  
Deviantd masternode status  
Deviantd getinfo  
```  

Also, if you want to check/start/stop **Deviant** , run one of the following commands as **root**:

```
DEVIANT_USER=deviant  #replace deviant with the MN username you want to check  
  
systemctl status $DEVIANT_USER #To check the service is running.  
systemctl start $DEVIANT_USER #To start Deviant service.  
systemctl stop $ADEVIANT_USER #To stop Deviant service.  
systemctl is-enabled $DEVIANT_USER #To check whetether Deviant service is enabled on boot or not.  
```  

***

  
Any donation is highly appreciated  

**DEV**: DAi2q5QtwxmQxhCFs8TpBkcCQ9uWZEZwc3  
**BTC**: 1BzeQ12m4zYaQKqysGNVbQv1taN7qgS8gY  
**ETH**: 0x39d10fe57611c564abc255ffd7e984dc97e9bd6d  
**LTC**: LXrWbfeejNQRmRvtzB6Te8yns93Tu3evGf  

