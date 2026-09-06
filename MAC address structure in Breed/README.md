[Support for Xiaomi Mi 3C | The principle of the MAC addresses in Breed](https://forum.openwrt.org/t/support-for-xiaomi-mi-3c/84973/402)
  
  
<p align="center">
<a href="#"><img src="/MAC address structure in Breed/Breed%20R3G%20MAC%20Stock%20En.png" width="800"</a>  

<p align="center">
<a href="#"><img src="/MAC address structure in Breed/Breed%20R3G%20MAC%20Keenetic%20En.png" width="800"</a>  

-------------------

<p align="center">
<a href="#"><img src="/MAC address structure in Breed/Breed%20R3G%20MAC%20Stock%20Ru.png" width="800"</a>  

<p align="center">
<a href="#"><img src="/MAC address structure in Breed/Breed%20R3G%20MAC%20Keenetic%20Ru.png" width="800"</a>  


**Standard MAC address structure**
```
RF1
WLAN MAC : EC-41-11-22-3C-6D The last value is the number in hexadecimal format following the number in the MAC address from the sticker
MAC1     : FD-9B-FF-FF-FF-FF
MAC2     : FF-FF-FF-FF-FF-FF

RF2
WLAN MAC : EC-41-11-22-3C-6E The last value is the number in hexadecimal format following the number in RF1 WLAN MAC
MAC1     : FD-9B-FF-FF-FF-FF
MAC2     : FF-FF-FF-FF-FF-FF

Independent parameters of RT6855/RT6856/MT7621
LAN MAC  : EC-41-11-22-3C-6B The last value is the number in hexadecimal format preceding the number in the MAC address on the sticker
WAN MAC  : EC-41-11-22-3C-6C MAC address from the sticker
```
**MAC address structure in the ported Keenetic firmware**
```
RF1
WLAN MAC : EC-41-11-22-3C-6C MAC address from sticker = RT6855/RT6856/MT7621 WAN MAC
MAC1     : EC-41-11-22-3C-FD The last value is the hexadecimal number following the MAC address on the sticker (RT6855/RT6856/MT7621 WAN MAC = RF1 WLAN MAC)
MAC2     : FF-FF-FF-FF-FF-FF

RF2
WLAN MAC : EC-41-11-22-3C-6E The last value is the number in hexadecimal format following the number in RF1 MAC1
MAC1     : FD-9B-FF-FF-FF-FF
MAC2     : FF-FF-FF-FF-FF-FF

Independent parameters of RT6855/RT6856/MT7621
LAN MAC  : EC-41-11-22-3C-6B The last value is the number in hexadecimal format preceding the number in the MAC address on the sticker
WAN MAC  : EC-41-11-22-3C-6C MAC address from the sticker = RF1 WLAN MAC
```
------------------
**Стандартная структура MAC-адресов**
```
RF1
WLAN MAC : EC-41-11-22-3C-6D Последнее значение - число в шестнадцатеричном формате следующее после числа в MAC-адресе с наклейки
MAC1     : FD-9B-FF-FF-FF-FF
MAC2     : FF-FF-FF-FF-FF-FF

RF2
WLAN MAC : EC-41-11-22-3C-6E Последнее значение - число в шестнадцатеричном формате следующее после числа в RF1 WLAN MAC
MAC1     : FD-9B-FF-FF-FF-FF
MAC2     : FF-FF-FF-FF-FF-FF

Independent parameters of RT6855/RT6856/MT7621
LAN MAC  : EC-41-11-22-3C-6B Последнее значение - число в шестнадцатеричном формате предшествующее числу в MAC-адресе с наклейки
WAN MAC  : EC-41-11-22-3C-6C MAC-адрес с наклейки
```


**Структура MAC-адресов в портированой прошивке Keenetic**
```
RF1
WLAN MAC : EC-41-11-22-3C-6C MAC-адрес с наклейки = RT6855/RT6856/MT7621 WAN MAC
MAC1     : EC-41-11-22-3C-FD Последнее значение - число в шестнадцатеричном формате следующее после числа в MAC-адресе с наклейки (RT6855/RT6856/MT7621 WAN MAC = RF1 WLAN MAC)
MAC2     : FF-FF-FF-FF-FF-FF

RF2
WLAN MAC : EC-41-11-22-3C-6E Последнее значение - число в шестнадцатеричном формате следующее после числа в RF1 MAC1
MAC1     : FD-9B-FF-FF-FF-FF
MAC2     : FF-FF-FF-FF-FF-FF

Independent parameters of RT6855/RT6856/MT7621
LAN MAC  : EC-41-11-22-3C-6B Последнее значение - число в шестнадцатеричном формате предшествующее числу в MAC-адресе с наклейки
WAN MAC  : EC-41-11-22-3C-6C MAC-адрес с наклейки = RF1 WLAN MAC
```
