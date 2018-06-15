開始吧!
===
1. 首先希望大家都可以擁有自己的[GitHub](https://github.com/)和[Docker Hub](https://hub.docker.com/)，這樣以後共同開發會方便很多<br>
2. 下方資料部分參考下方所有連結
3. 一切教學皆為學術目的
---
目錄
* [網路攻擊](#網路攻擊)
    * [網路滲透作業系統(Kali Linux)](#一網路滲透作業系統kali-linux)
    * [搜尋引擎滲透(Google Hacking)](#二搜尋引擎滲透google-hacking)
* [程式開發](#程式開發)
    * [基礎程式語言(python)](#一基礎程式語言python)
* [虛擬化](#虛擬化)
    * [基礎虛擬化技術(Docker)](#一基礎虛擬化技術docker)
    * [基礎虛擬化技術(VMware)](#二基礎虛擬化技術vmware)
* [資料庫](#資料庫)
    * [基礎資料庫(Mongo)](#一基礎資料庫mongo)
    * [基礎資料庫(MySQL)](#二基礎資料庫mysql)
---
# 網路攻擊

## 一、網路滲透作業系統(Kali Linux)
* [Kali Linux 官方](https://www.kali.org/)
    下載Kali
* [Docker版 Kali Linux](https://hub.docker.com/r/kalilinux/kali-linux-docker/)
    如果常用Docker的人可以試試，但工具部分沒有其他版本那麼齊全
### 小問題
* 如何開啟Kail後自動登入桌面
  - 輸入 `vi /etc/gdm3/daemon.conf`
  - 將 `#AutomaticLoginEnable = True` 和 `#AutomaticLogin = root` 的 # 刪除
* 如何設定SSH遠端登入
  - 輸入 `vi /etc/rc.local`
  - 增加 `/etc/init.d/ssh start`
  - 輸入 `vi /etc/ssh/sshd_config`
  - 修改 `PermitRootLogin without-password` 為 `PermitRootLogin yes`
---
## 二、搜尋引擎滲透(Google Hacking)
* [宅學習 - Social Learning Space](https://sls.weco.net/node/12922)
    裏頭有非常多常用的手法可以應用在滲透上
* [GoogleHacking基礎](http://www.vixual.net/blog/archives/152)
    裏頭有非常多常用的手法可以應用在滲透上
* [exploit-db實戰範例](https://www.exploit-db.com/google-hacking-database/)
    裏頭有非常多常用的手法可以應用在滲透上
* [信息收集篇————Google Hacking](https://blog.csdn.net/Fly_hps/article/details/79404270)
    裏頭有非常多常用的手法可以應用在滲透上
* 基礎指令介紹
  - site: (搜尋特定網址)
  - inurl: (搜尋特定連結)
  - intext: (搜尋網頁內文字)
  - intitle: (搜尋網頁標題)
  - filetype  |  ext  : (搜尋特定檔案格式)
  - link: (搜尋互相連結的網頁)
  - cache: (顯示網頁在Google中的暫存資料)
  - info: (列出某網站在Google上存有哪些資訊)
* 常用指令集
  - inurl:admin
  - inurl:phpinfo.php
  - intitle:index of 學生證
---
# 程式開發

## 一、基礎程式語言(python)
* [Python官方](https://www.python.org/)
    下載python
* [菜鳥教程](http://www.runoob.com/python/python-tutorial.html)
    不必看完，但要用的時候找的到
* [程式語言教學誌](http://kaiching.org/pydoing/python.html)
    不必看完，但要用的時候找的到
* [Python 基础入門教程](https://alleniverson.gitbooks.io/python2-course/content/)
    不必看完，但要用的時候找的到
* [《跟老齐学Python》（入门教程）](https://normanbb.gitbooks.io/test/content/)
    資料庫與EXCEL檔案的部份寫的很清楚，其他部份也相當完整
* [python 安全编程教程](https://wizardforcel.gitbooks.io/py-sec-tutorial/content/index.html)
    與滲透測試較有關係，算是較進階的部份
### 第三方函式庫

#### Paramiko
* [Paramiko官方](http://www.paramiko.org/)
   裏頭有所有的函式和最詳細的資料。
* [GitHub Paamiko](https://github.com/paramiko/paramiko)
   含所有的程式碼更新與原始碼。
* [GitBook python Paramiko(模仿SSH交互且執行指令)](http://python.jqlinux.com/pythonchang-yong-di-san-fang-3001-nei-zhi-mo-kuai/python-paramikomo-fang-ssh-deng-lu-zhi-xing-ming-4ee429.html)
   如標題，內容主要為SSH連線相關範例。
### 小問題
* pip安裝
  - 下載[get-pip.py](https://bootstrap.pypa.io/get-pip.py)
  - 開啟cmd執行 `python get-pip.py`
  - 最後加入 `C:\Python27\Scripts` 到環境變數中
### 測驗
    請練習菜鳥教程-100例中第1、3、8、24、26、32、34、61、71、83、85、88、97和100題。
---
# 虛擬化

## 一、基礎虛擬化技術(Docker)
* [Docker —— 從入門到實踐](https://philipzheng.gitbooks.io/docker_practice/content/)
    請看完 Docker簡介、基本概念、安裝、映像檔、容器、倉庫和Dockerfile，其他不必看完，但要用的時候找的到
* [Docker Hub](https://hub.docker.com/)
    目前由Docker官方維護的公共倉庫 Docker Hub，且Docker Hub 中可直接下載他人或官方的映像檔來使用
### 小問題
* 關於Docker下的alpine
  - alpine原本並沒有bash，所以要遠端登入時可使用sh來遠端登入
* docker-compose up leads to “client and server don't have same version” error but client and server have the same version
  - https://cutejaneii.wordpress.com/2017/06/19/docker-8-%E5%8D%87%E7%B4%9Adocker/
### 測驗
    請使用Docker建立一個FTP伺服器在Ubuntu中
---
## 二、基礎虛擬化技術(VMware)
* [VMware官方](https://www.vmware.com)
    下載VMware(有付費版及免費版)
* [虛擬機器VMware Workstation Pro 14下載與安裝](http://blog.xuite.net/yh96301/blog/63322621-%E8%99%9B%E6%93%AC%E6%A9%9F%E5%99%A8VMware+Workstation+Pro+14%E4%B8%8B%E8%BC%89%E8%88%87%E5%AE%89%E8%A3%9D)
    此篇Blog有關於下載與安裝的介紹等
### 小問題
* 於Ubuntu 中 VMtools 跳出錯誤訊息 VMware Tools installation cannot be started manually while Easy Install is in progress.
  - 開啟terminal執行 `apt -y --reinstall install open-vm-tools-desktop fuse`
* 版本不相同而導致無法開啟
  - 只需用記事本打開虛擬機目錄下的 .vmx 文件，並將 virtualHW.version ="7" 中的數字改為虛擬機的版本即可。
---
# 資料庫

## 一、基礎資料庫(Mongo)
* [DockerHub mongo](https://hub.docker.com/_/mongo/)<br>
    裏頭有關於mongo與mongo-express的compose.yml，如果你已經學會docker，非常建議直接使用。
* [mongo 入門指南](https://jockchou.gitbooks.io/getting-started-with-mongodb/content/)
    簡單且完整教學，主要是如何操作mongo的基本指令，實用性非常高，必看也必會。
* [MongoDB 學習教程](https://piaosanlang.gitbooks.io/mongodb/content/)
    較為進階，有很多關於其他資料庫的比較，如果要深入mongodb，這個gitbook很值得參考。
### 小問題
* 跳出錯誤訊息 not authorized on admin to execute command { listDatabases: 1.0, $db: \"admin\" }
  - 輸入指令 `mongo`
  - 輸入指令 `use admin`
  - 輸入指令 `db.auth('root','example')`
---
## 二、基礎資料庫(MySQL)
* [MySQL 超新手入門（1）重新開始](http://www.codedata.com.tw/database/mysql-tutorial-getting-started)
    這是新手必看的Blog，整理的很完整了。
* [MySQL基礎筆記](https://cxiaodian.gitbooks.io/mysql/content/index.html)
    安裝、設定到基礎SQL語法都很完整。
* [mysql5.7官方文檔翻譯](https://404dream.gitbooks.io/mysql/content/)
    翻譯官方文件的第四和五章的部分，不想看英文的可以來看看。
### 小問題
* 跳出錯誤訊息 mysql ERROR 1130: Host '*****' is not allowed to connect to this MySQL server
  - [宇若彎彎-連接遠端MYSQL ERROR 1130解決辦法](http://s90304a123.pixnet.net/blog/post/39306139-mysql-error-1130)
---
### 開發中...
