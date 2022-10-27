<p style="font-size:14px" align="right">
<a href="https://t.me/PemulungAirdropID" target="_blank">Join our telegram <img src="https://user-images.githubusercontent.com/72949170/194228482-0f875615-e155-4b12-8716-8111addd6cba.jpg" width="30"/></a>
</p>

# SCROLL TUTORIAL (NODE)

## 1. Update sesajen dulu
```
apt install update
```

```
apt install upgrade
```

Install git kalau belum install

```
apt install git
```

![image](https://user-images.githubusercontent.com/72949170/198203337-555136d0-bf75-4886-83bc-dc0696b0938e.png)


## 2. Install nodeJS + NPM (kalau belum)

```
sudo apt install nodejs
```

```
sudo apt install npm
```

![image](https://user-images.githubusercontent.com/72949170/198203659-e4d5eb6d-032a-4586-a091-2d6048551fb8.png)


## Deploy Contract (Disini gw pake Foundry)
- Clone repo
```
git clone https://github.com/scroll-tech/scroll-contract-deploy-demo.git
cd scroll-contract-deploy-demo
```

- Install Foundry
```
curl -L https://foundry.paradigm.xyz | bash
```

```
foundryup
```

- Deploy
```
forge create --rpc-url https://prealpha.scroll.io/l2 \
  --value <lock_amount> \
  --constructor-args <unlock_time> \
  --private-key <your_private_key> \
  --legacy \
  contracts/Lock.sol:Lock
```

*Ga pake <>*


<lock_amount> : Buat jumlah token yang lu mao lock misal (0.0000001ether)

<unlock_time> : Sampe kapan lock nya, tanggal nya diganti jadi bentuk unix timestamp https://www.unixtimestamp.com/, misal (1669761200), artinya Nov 29 2022 

![image](https://user-images.githubusercontent.com/72949170/198204614-beb19e18-3643-4f7b-9984-06dc4de56c0e.png)


## Done
