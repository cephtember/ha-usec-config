

# **Neocaine Home Assistant Configuration**

**TODO**
* Переделать логику автоматизаций света MQTT на нажатие клавиш выключателя (Сделать как в Баре)
* Исправить все deprecated функции и сенсоры

**Home Assistant** - это open-source платформа для автоматизации, работающая на Python 3. Позволяет отслеживать и контролировать все устройства в доме и автоматизировать действия. Идеально может работать на одноплатном компьютере Raspberry PI. Так же может работать на платформах Windows, Linux. Интерфейс построен через браузер работа возможно на любом устройстве Android, iOS.

Ниже предоставлены все устройства и компоненты, используемые в моем умном доме.

**Содержание**
* [Климат контроль](#климат-контроль)
    * [Жалюзи](#жалюзи)
    * [Отопление и Кондиционирование](#отопление-и-кондиционирование)
    * [Разное](#разное)
* [Освещение и розетки](#освещение-и-розетки)
    * [Освещение](#освещение)
    * [Розетки](#розетки)
* [Датчики и безопасность](#датчики-и-безопасность)
    * [Камеры и домофоны](#камеры-и-домофоны)
    * [Датчики температуры](#датчики-температуры)
    * [Датчики открытия](#датчики-открытия)
    * [Датчики безопасности](#датчики-безопасности)
* [Аудио / Видео](#аудио-и-видео)
    * [Телевидение и стриминг](#телевидение-и-стриминг)
* [Компоненты умного дома](#компоненты-умного-дома)
    * [Home Assistant Железо](#home-assistant-железо)
    * [Home Assistant Software](#home-assistant-софт)
    * [Голосовое управление](#голосовое-управление)
    * [Сетевая инфраструктура](#сетевая-инфраструктура)
    * [Lovelace UI Скриншоты](./LovelaceUI.md)
* [Благодарности](#Благодарности)

# Климат контроль

## Жалюзи

| <a href="https://www.ikea.com/gb/en/p/fyrtur-block-out-roller-blind-wireless-battery-operated-grey-30408173/"> FYRTUR roller blind </a> | <a href="https://www.ikea.com/gb/en/p/fyrtur-block-out-roller-blind-wireless-battery-operated-grey-30408173/"> TRADFRI open/close remote </a> | <a href="https://www.ikea.com/gb/en/p/fyrtur-block-out-roller-blind-wireless-battery-operated-grey-30408173/"> TRADFRI signal repeater </a>|
| --- | --- | --- |
|  <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/fyrtur.jpg" width="200"/> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/tradfriremote.jpg" width="200"/> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/tradfrisignal.jpg" width="200"/>

## Отопление и Кондиционирование

| <a href="https://www.zigbee2mqtt.io/devices/BHT-002-GCLZB.html"> 	Moes BHT series Thermostat </a> | <a href="https://www.midea.com/gulf/product/Residential-AC/Split-AC/Mission-Inverter-12K"> Midea Mission AC </a>    | Электро-полотенцесушитель     | <a href="https://www.zigbee2mqtt.io/devices/TS011F_plug.html"> Tuya Smart plug </a>
| --- | --- | --- | --- |
|  <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/moesthermostat.jpg" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/mideamission.jpg" width="200"/> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/electrotherm.jpg" width="200"/> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/tuya_smartplug.jpg" width="200" /> |

## Разное
| Xiaomi 1C | Xiaomi Purifier 3 | Xiaomi Smart Humidifier |
| --- | --- | --- |
| <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/xiaomi1c.jpg" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/xiaomiAirpurifier3.jpg" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/smartSterilizationHumidifier.jpg" width="200" /> |

# Освещение и розетки

## Освещение

| <a href="https://www.yeelight.com/"> Yeelight YLXD54YL </a> | <a href="https://www.yeelight.com/"> Yeelight YLXD05YL </a> | <a href="https://www.yeelight.com/"> Yeelight YLXD01YL </a> | <a href="https://www.yeelight.com/"> Yeelight YLDD04YL </a>
| --- | --- | --- | --- |
| <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/yeelight_YLXD54YL.png" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/yeelight_galaxy_seiling_lamp_480mm.jpg" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/yeelight_small.jpg" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/yeelight%20strip.jpg" width="200" /> |

| <a href="https://www.zigbee2mqtt.io/devices/WXCJKG11LM.html#xiaomi-wxcjkg11lm"> Aqara Opple switch </a> | <a href="https://www.zigbee2mqtt.io/devices/WXCJKG11LM.html#xiaomi-wxcjkg11lm"> Aqara wireless switch </a> | <a href="https://www.zigbee2mqtt.io/devices/WXKG01LM.html#xiaomi-wxkg01lm"> MiJia wireless switch </a> | <a href="https://www.zigbee2mqtt.io/devices/MFKZQ01LM.html#xiaomi-mfkzq01lm"> Aqara Cube </a> |
| --- | --- | --- | --- |
| <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/aqara_opple.jpg" width="200"/> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/xiaomiAqaraWirelessSwitch.jpg" width="200"/> | <img src="https://github.com/neocaine/ha-usec-config/blob/main/www/images/logo/xiaomiMijiaWirelessSwitch.jpg" width="200"/> | <img src="https://github.com/neocaine/ha-usec-config/blob/main/www/images/logo/aqara_cube.jpg" width="200"/> |

| MoesHouse WS-EUY1-W | MoesHouse WS-EUY2-W | MoesHouse WS-EUY3-W | Lonsonho QS-Zigbee-D02-TRIAC-LN |
| --- | --- | --- | --- |
| <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/moes1Gang.jpg" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/moes2Gang.PNG" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/moes3Gang.jpg" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/lonsonhodimmer.jpg" width="200" /> 

## Розетки

| <a href="https://www.moeshouse.com/collections/smart-socket/products/wifi-de-smart-socket-freely-removable-detachable-from-wall-plate-smart-life-tuya-app-remote-control-work-with-alexa-google-home"> MoesHouse Smart Socket </a> | <a href="https://www.moeshouse.com/collections/switch-module"> MoesHouse Zigbee Switch </a> | <a href="https://www.zigbee2mqtt.io/devices/TS011F_plug.html"> Tuya Smart plug </a> |
| --- | --- | --- |
| <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/moesPlug.PNG" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/moesNoneutralSwitch.jpg" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/tuya_smartplug.jpg" width="200" /> |

| Sonoff S55 | Sonoff Mini | Sonoff BazicZBR3 |
| --- | --- | --- |
| <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/sonoffS55.webp" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/sonoff_mini.jpg" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/sonoffBazicZbr3.png" width="200" /> |

# Датчики и безопасность

## Камеры и домофоны

| <a href="https://www.hikvision.com/my/products/Video-Intercom-Products/Doorbells/Pro-Series/DS-KB8112-IM/"> Hikvision DS-KB8112-IM </a> | <a href="https://www.hikvision.com/en/products/Video-Intercom-Products/IP-Series/Pro-Series/ds-kh8520-wte1/"> Hikvision DS-KH8520-WTE1 </a> | <a href="https://www.hikvision.com/mena-en/products/IP-Products/Network-Cameras/Value-Series/DS-2CD1143G0-I/"> Hikvision DS-2CD1143G0-I </a> |
| --- | --- | --- |
| <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/hikvisionCallPanel.PNG" width="200"/> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/hikvisionPanel.PNG" width="200"/> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/hikvisionCamera.PNG" width="200"/> |

## Датчики температуры

| <a href="https://sonoff.tech/product/smart-home-security/snzb-02/"> Sonoff SNZB-02 </a> | <a href="https://www.aqara.com/en/temperature_humidity_sensor.html"> Aqara WSDCGQ11LM </a> |  
| --- | --- | 
| <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/sonoffSNZB02.PNG" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/aqaraTemperatureAndHumidity.jpg" width="200" /> |


## Датчики открытия

| <a href="https://www.aqara.com/en/door_and_window_sensor.html"> Aqara MCCGQ11LM </a> |
| --- |
| <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/aqaraWindowsAndDoors.PNG" width="200" /> |

## Датчики безопасности

| <a href="https://www.zigbee2mqtt.io/devices/TS0204.html"> CR Gas sensor TS0204 </a> | <a href="https://www.zigbee2mqtt.io/devices/TS0205.html"> CR Smoke sensor TS0205 </a> | <a href="https://www.aqara.com/en/water_sensor.html"> Aqara SJCGQ11LM  </a> | <a href="https://www.zigbee2mqtt.io/devices/RTCGQ11LM.html#xiaomi-rtcgq11lm"> Xiaomi RTCGQ11LM  </a> |
| --- | --- | --- | --- |
| <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/CRGas.jpg" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/CRSmoke.jpg" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/aqaraWaterLeak.PNG" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/aqara_motion_sensor.jpg" width="200" /> 


# Аудио и Видео

## Телевидение и стриминг

| <a href="https://www.sony.ru/electronics/support/televisions-projectors-lcd-tvs-android-/kd-49xh8096/specifications"> Sony KD-49XH8096 </a> | <a href="https://www.xbox.com/"> Xbox Series X </a> | <a href="https://www.edifier.ru/shop/speakers/s3000pro/"> Edifier S3000 Pro </a> | <a href="https://www.apple.com/ru/apple-tv-4k/"> Apple TV (2021) </a> |
| --- | --- | --- | --- |
| <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/sony_kd-49XH8096.jpg" width="200"/> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/xbox_series_x.png" width="200"/> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/edifier.webp" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/appletv.png" width="200" />

# Компоненты умного дома

## Home Assistant Железо

| <a href="https://www.argon40.com/argon-one-m-2-case-for-raspberry-pi-4.html"> Argon ONE M.2 Case </a> | <a href="https://www.raspberrypi.org/products/raspberry-pi-4-model-b/"> Raspberry Pi 4 </a> | <a href="https://smartlight.me/ustroystva-umnogo-doma/zigbee-ustroistva/zigbee-koordinator-v4-cc2652p"> USB v4 CC2652P </a> | <a href="https://shop.westerndigital.com/ru-ru/products/network-attached-storage/wd-my-cloud-expert-series-ex2-ultra#WDBVBZ0040JCH-EESN"> My Cloud EX2 </a> |
| --- | --- | --- | --- |
| <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/argonone.jpg" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/raspberrypi.png" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/cc2652p.jpg" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/mycloud.webp" width="200" /> |

## Home Assistant Софт

| <a href="https://www.home-assistant.io/"> Home Assistant Core </a> | <a href="https://www.docker.com/"> Docker </a> | <a href="https://mosquitto.org/"> MQTT Server </a> | <a href=""> Zigbee2MQTT </a> |
| --- | --- | --- | --- |
| <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/homeassistant.png" width="200"/> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/docker.jpg" width="200"/> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/mosquitto.png" width="200"/> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/zigbee2mqtt.png" width="200"/> |

| <a href="https://www.samsung.com/ru/apps/smartthings/"> Samsung SmartThings </a> | <a href="https://volumio.com/en/"> Volumio </a> | <a href="https://spotify.com"> Spotify </a> | <a href="https://telegram.org"> Telegram </a> |
| --- | --- | --- | --- |
| <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/smartthings.png" width="200" />| <img src="https://github.com/neocaine/ha-usec-config/blob/main/www/images/logo/volumio.png" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/spotify.webp" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/telegram.jpg" width="200" /> |

## Голосовое управление

| Google Assistant | Plex Assistant |
| --- | --- |
|  <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/google_assistant.jpg" width="200"/> |  <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/plex_assistant.jpg" width="200"/> | 

## Сетевая Инфраструктура

| Mikrotik AC3 | Mikrotik AC2 | Hikvision DS-3E0105P-E/M |
| --- | --- | --- |
| <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/mikrotikAC3.jpeg" width="200" /> | <img src="https://github.com/neocaine/ha-usec-config/blob/main/www/images/logo/mikrotikAC2.PNG" width="200" /> | <img src="https://raw.githubusercontent.com/neocaine/ha-usec-config/main/www/images/logo/hikvision3e0105p_eb.png" width="200" /> |

## Lovelace UI
Скриншоты Lovelace UI можно посмотреть здесь: [Lovelace UI Screenshots](./LovelaceUI.md)

# Благодарности
Разметка и идея файла README.md взята с репозитория [DrJohnT](https://github.com/DrJohnT/HomeAssistantPublicConfig).
