# YIP
### Youth Internet Punisher
---

A tool that allows you to punish young fuc*ers by managing your home router configuration.

## Requirements

As of now, this tool works only with routers from the **Claro** ISP. A model called `HGB10R-02`

You can check your model by accessing the router's web interface, and looking at the inspector's console.

![Screenshot](https://user-images.githubusercontent.com/2521595/219724214-336e6601-e538-4c50-adf5-b72484c87d94.png)

## Configuration
Put the `.yip.json` inside your `$HOME` folder and configure the credentials used to access your router.
You can check your browser inspector to retrieve your username and password used to authenticate.

## Usage

## Command Line

### List devices connected to the DHCP
```shell
$ yip listDevices
```

Will output all devices connected to the DHCP, with their mac address, and their hostname.

```bash
===== DEVICES =====
64:64:4A:39:E3:38 - MiWiFi-R4CM
24:A1:60:3F:51:37 - ESP_3F5137
F8:54:B8:94:C5:24 - XBOX <- aka. The victim
64:A2:00:01:E8:6B - RedmiNote8-RedmiNote
88:66:5A:1E:AA:38 - BR0C02FM02JMD6M
===================
```

### Adds a mac address to the blacklist (aka. the naughty list)
```shell
$ yip filterMac 64:A2:00:01:E8:6B 24:A1:60:3F:51:37 ...
```

### Removes a mac address from the blacklist
```shell
$ yip unfilterMac 64:A2:00:01:E8:6B 24:A1:60:3F:51:37 ...
```

## Telegram Bot

![Screenshot](https://user-images.githubusercontent.com/2521595/219872250-002c8077-7991-4ee1-8b69-1c84f47cf292.png)

You can also run a telegram bot to listen to your commands so you can trigger the client from anywhere.

Run it with

```shell
$ yip telegramBot
```

*In order to be able to execute commands you should login using the `telegram.password` set on the config* <br/>
```shell
/login [PASSWORD]
```
