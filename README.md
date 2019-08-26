# tellus

## apache2 기본 보안 설정 ##
```
sudo sed -i "s/Options Indexes FollowSymLinks/Options FollowSymLinks/g" /etc/apache2/apache2.conf
cat /etc/apache2/apache2.conf | grep 'Directory /var/www/' -A4
sudo sed -i "s/ServerTokens OS/ServerTokens Prod/g" /etc/apache2/conf-enabled/security.conf
grep "ServerTokens Prod" /etc/apache2/conf-enabled/security.conf
sudo sed -i "s/ServerSignature On/ServerSignature Off/g" /etc/apache2/conf-enabled/security.conf
grep "ServerSignature Off" /etc/apache2/conf-enabled/security.conf
```

## email, name 설정 ##
```
git config --global user.email "skuTellus@gmail.com"
git config --global user.name "tellus"
```
## 클론 및 웹 디렉토리 설정 ##
```
cd $HOME
git clone https://github.com/dydgns2017/tellus
sudo ln -s $HOME/tellus /var/www/tellus
```
