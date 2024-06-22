# Host nodejs app lên server linux

## A. Cài đặt môi trường

### 1. Node version manager
```shell
# Cai dat node version manager
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash

# Cai dat nodejs su dung nvm, su dung phien ban nao thi cai phien ban do
# cai dat version 16
# nvm install 16
# cai dat version 20
nvm install 20

# verifies the right Node.js version is in the environment
node -v # should print v20.x.x

# verifies the right NPM version is in the environment
npm -v # should print 10.x.x
```
### 2. Sử dụng PM2 để chạy và quản lý hosting cho nodejs app
```shell
# Cai dat PM2, chu y su dung node version bao nhieu thi PM2 se duoc
# cai dat theo node version do

# VD: Nodejs app su dung node v20, chuyen sang node version 20
nvm use 20

# Cai dat PM2
npm install pm2 -g

# Verify pm2 version
pm2 --version

# Tao folder chua app, goi y nen tao app trong folder /var/www/
cd /var/www
mkdir my_app
cd my_app

# Dung PM2 de host app
# `pm2 start "command_start_app" --name ten_app --log-date-format "DD-MM-YYYY HH:mm Z" --update-env`
# VD: de chay nodejs chay lenh `npm start`, ten app la Demo, thi chay lenh
pm2 start "npm start" --name "Demo" --log-date-format "DD-MM-YYYY HH:mm Z" --update-env

# Luu lai danh sach process, de phong truong hop he thong khoi dong lai
# thi khong bi mat, va PM2 se tu khoi dong lai app
pm2 save
```
