# Scrypta Crowdfunding PoC

The goal of this PoC is to create a crowdfunding campaign that will raise money in BTC/LYRA/EUR and will create the equivalent in the main asset.
At the end of the process the owner will receive the funding asset (BTC/LYRA/EUR) that will be used as below of the main asset. 
This asset will be distributed to the beneficiars of the token itself. It's simple to understand the the main asset is linked to the funding asset so we'll assume that every asset will be exchanged into a stable coin.

This is an experiment to expand the purpose of the project "Social Pay", so anyone can send helps directly to the administration so to the people with the transparency needed for operations like this.

Please note: this repository can be used to raise money so please be sure (if you want to use it) that you can do it in legal terms. In this concept we'll not raise true money but we'll use testnet assets.

## Abstract

The idea is simple, we want to sell our tokens without pre-create it and, when the token is successfully created we want to receive two kind of assets, the first is the funding asset itself (LYRA, BTC etc) and the second asset is the Planum one, that we'll be sent to the beneficiars. 

We mentioned two different planum sidechains above because the third asset is the "Proof of Funding" so the user will receive an asset that represent its donation.

So let's give names to this assets to be 100% clear:
- Main asset: sEUR 
- Funding asset: BTC
- Proof asset: hEUR

The entire flow is: 
1) The user want to donate (for ex.) 1 BTC to the project
2) The backend creates a new BTC address
3) The user send BTC to the address and the backend validate it
4) The backend will exchange the BTC and creates the equivalent in hEUR, for example 7.122,00 hEUR
5) The user will receive this asset
6) The backend issues 7.122,00 sEUR on the main sidechain (this operation can be done even manuallly)

As we can see the process is pretty simple, we use two different sidechains for two reasons: 
1) Traceabilty: anyone will know how much the project raises
2) Security: the process is automatic so we need to create an "hot chain" that can be exposed and has intrinsic value 0