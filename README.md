# tron_wallet_android
a tron wallet android 






![Pra](https://github.com/Prochain/tron_wallet_android/raw/master/pic/pra.png)

![Pra](https://github.com/Prochain/tron_wallet_android/raw/master/pic/tron.png)







1.在android 兼容运行了wallet cli， 包含了cli的大部分功能函数， 导入创建， 转账，查询，备份，等


2. 添加了contract 调用， 可以在android手机里调用tron中的合约函数和做合约交互


3. todo，添加js中间件， 可以做h5浏览器打开后与钱包交互









This is Android tron wallet base on the tron wallet cli by JAVA.
Support most of the wallet cli function

create or import key.
checkBalance or assets. 
transfer 
call dapp contract, 
backup private key




1. About Tron

https://github.com/tronprotocol

https://tron.network/


TRON is an ambitious project dedicated to the establishment of a truly decentralized Internet and its infrastructure.

The current TRON team radiates out from Beijing to Seoul, Tokyo, San Francisco and many other countries and regions, totaling more than 100 members. The technological backbones of TRON are experienced blockchain enthusiasts who were previously employed by internet giants such as Alibaba, Tencent and Baidu.



=============================================

2. Usage


You can check the testCenter's sample for more functions.



 private void changeWalletPwd()
{

WalletApiWrapper walletApi = new WalletApiWrapper();

walletApi.context = this;

   //then you can call wallApi's function ....

}


ImportWallet

ImportwalletByBase64

ChangePassword

Login

Logout

BackupWallet

BackupWallet2Base64

Getaddress

GetBalance

GetAccount

GetAssetissueByAccount

GetAssetIssueByName

SendCoin

TransferAsset

ParticipateAssetissue

Assetissue

CreateWitness

VoteWitness

FreezeBalance 

UnfreezeBalance

WithdrawBalance

Listaccounts

Listwitnesses

Listassetissue

listNodes

GetAssetIssueByName


Getblock UpdateAccount  Exit or Quit



================================================

3. call or sign contract




 private void callSignContract()
 {
        if (walletApi==null)
        {
            Log.d("wallet", "please login first");
            return ;
        }

        String contractAddress = "THBE7KgFSP6zWrfJh7yp4gfZd9VCfPcbws";

        String method = "click";
        String params = "1";

        String privateKey = "Your private key";
        walletApi.ecKey = ECKey.fromPrivate(ByteArray.fromHexString(privateKey));
        //ClickEvent
        walletApi.triggerContract(contractAddress,method, params);


    
 }
    
    
===================================================


4. dapp interaction relate. 

todo....using the similar js middle ware as we do in EOS






