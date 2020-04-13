# Corona Notifier 

![GitHub ](https://img.shields.io/github/last-commit/ahmadchen/CoronaNotifier)
![Twitter](https://img.shields.io/twitter/follow/teman_bahagia?style=social)

Corona Notifier is a Whatsapp automatic notification robot using MQTT & nodeJS. The Corona Service will collect latest data about the COVID-19 indonesian case from [indonesia-covid-19-api](https://indonesia-covid-19.mathdro.id/api) by [mathdroid](https://github.com/mathdroid/indonesia-covid-19-api)

#### The Diagram
![Diagram](Diagram.png)


## Getting Started

This project require MQTT broker, nodeJS

Clone this project

```bash
> git clone https://github.com/ahmadchen/CoronaNotifier.git
> cd CoronaNotifier

```

Install the dependencies:

```bash
> npm i
```

Edit MQTT topic in .env file:

```
MQTT_TOPIC= ....
```

run the Whatsapp bot

```bash
> node index.js
```

after running it you need to scan the qr

run the corona service

```bash
> node CoronaService\corona.js
```

## Bot Whatsapp Command
(WARNING: This is only available with Bahasa Language)

This bot is for covid-19 information purpose by automatically answer for available data, by using the available command :
1. !help 
The introduction and list of available command, example output
```
COVID-19 
!corona  =>  ........
!aktif  =>  .......
!mati  =>  ......
```
2. !ping 
Using this command will response "pong"
3. !corona 
Using this command will return information about current indonesia corona case and global case, example output
```
         COVID-19 Update!!
Negara: xx

Total Kasus: xx
Kasus Baru: xx
Total Pasien: xx

Sembuh: xx
Sembuh Baru: xx
Presentase Sembuh: xx.xx%

Meninggal: xx
Meninggal Baru: xx
Presentase Meninggal: xx.xx%

Dicek pada: xxx, xx xxxx 2020 | xx.xx WIB
```
4. !aktif 
Using this command will enable notifications when there is a data update.
5. !mati 
Using this command will disable notifications when there is a data update.
6. !data
Using this command will return a list of websites that contain coronavirus data.
7. !peta 
Using this command will return the corona virus distribution map information.
