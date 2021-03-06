# How to use

## environment
### carthage
* Download latest carthage from https://github.com/Carthage/Carthage/releases
### xcode setting
* Select proper command line tool from Xcode > Preferences > Locations 
* Disable bitecode at build settings.

## Cartfile
To use NRLWalletSDK, need to make Cartfile at the root folder of your project.

```
github "krzyzanowskim/CryptoSwift"
github "attaswift/BigInt" ~> 3.0
github "Boilertalk/Web3.swift"
github "Alamofire/Alamofire" ~> 4.7
github "Hearst-DD/ObjectMapper" ~> 3.2
github "SwiftyJSON/SwiftyJSON" ~> 4.0
github "gedanziger/nrlwallet-ios-sdk"
```
## Update Carthage
Once you made cartfile, you can now update carthage.
>carthage update --platform iOS 

## Embed frameworks
After update carthage, now you can embed frameworks to your target.

* Select target to integrate with NRLWalletSDK.
* General tab and go to Embedded Binaries section.
* Push plus button and import frameworks which was made from carthage.

Now you can use NRLWalletSDK!


# Dependency libraries

## Carthage

* make Cartfile at the root folder of project
```
github "krzyzanowskim/CryptoSwift"
github "attaswift/BigInt" ~> 3.0
github "Boilertalk/Web3.swift"
github "Alamofire/Alamofire" ~> 4.7
github "Hearst-DD/ObjectMapper" ~> 3.2
github "SwiftyJSON/SwiftyJSON" ~> 4.0
github "gedanziger/nrlwallet-ios-sdk"
```
* run following command 
>carthage update --platform iOS --no-use-binaries

## framework
### neoutils.framework
>https://github.com/O3Labs/neo-utils
>need setting of bitcode disabled
>need to manually include from O3Labs
>to build neo-utils, need to install go and go-mobile


## included sources

### web3.swift

>https://github.com/Boilertalk/Web3.swift

### CocoaLumberjack (Libraries)

can be downloaded from BitcoinSPV pod. or 

>https://github.com/CocoaLumberjack/CocoaLumberjack

### secp256k1
>https://github.com/bitcoin-core/secp256k1
>need to add in Libraries manually

### BitcoinSPV (Libraries)
>https://github.com/keeshux/BitcoinSPV/
>need to add in Libraries manually

### openssl

can be downloaded from BitcoinSPV pod. or 

to libs of libssl and libcrypto should be explicitly included as linked library of NRLWalletSDK

>https://github.com/openssl/openssl
>need to add in Libraries manually

### loafwallet-core (Libraries)
>https://github.com/litecoin-foundation/loafwallet-ios
>only included loafwallet-core

### stellar-ios-mac-sdk
>https://github.com/Soneso/stellar-ios-mac-sdk
>only included part of this sdk, so need to update for each files


# Build Carthage framework

## build

### download dependences
>carthage update --platform iOS

### build project at xcode

### carthage build
>carthage build --no-skip-current
>carthage archive NRLWalletSDK

>git push   ---> this carthage can be used as global carthage file

## key / address test
### bitcoin, litecoin, ethereum
>https://iancoleman.io/bip39/

### neo
>https://coranos.github.io/neo/ledger-nano-s/recovery/

### stellar
>https://github.com/stellar/go/releases/  stellar-hd-wallet

## transaction test

### ethereum
* http://etherscan.io/
* http://ropsten.etherscan.io/

### bitcoin
* faucet: https://testnet.manu.backend.hamburg/faucet
* https://testnet.blockchain.info/

### litecoin
* https://live.blockcypher.com/ltc

### neo
* https://neotracker.io/

### stellar
* https://stellarchain.io/


