# uicapp

## 打包app
### cordova build android --release

# 打包发布版本
### java -jar "bundletool-all-1.12.1.jar" build-apks --mode=UNIVERSAL --bundle="app-release.aab" --output="release-app.apks"


# 签名生成20000天的密钥证书
### keytool -genkey -v -keystore uicapp.keystore -alias uicapp -keyalg RSA -validity 20000


# 打包并签名
### java -jar "bundletool-all-1.12.1.jar" build-apks --mode=UNIVERSAL --bundle="app-release.aab" --output="release-app.apks" --ks="uicapp.keystore" --ks-key-alias=uicapp