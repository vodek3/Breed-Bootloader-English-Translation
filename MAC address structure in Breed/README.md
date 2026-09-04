

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


The principle of the MAC addresses in Breed is the following:
https://forum.openwrt.org/t/support-for-xiaomi-mi-3c/84973/402



RF1
WLAN MAC : MAC address of the WiFi interface found on the sticker of the router
MAC1     : Same as WLAN MAC except the last digits (e.g. instead of C3 you can use C4)
MAC2     : Totally different to WiFi MAC address: E. g. 00-0C-43-AA-BB-CC

RF2
WLAN MAC : FF-FF-FF-FF-FF-FF
MAC1     : FF-FF-FF-FF-FF-FF
MAC2     : FF-FF-FF-FF-FF-FF

Independent parameters of RT6855/RT6856/MT7621
LAN MAC  : FF-FF-FF-FF-FF-FF
WAN MAC  : FF-FF-FF-FF-FF-FF

Про структуру MAC-адресов в Breed:
https://4pda.to/forum/index.php?showtopic=837667&st=36720#entry143653965
------------------------------------------------------
Стандартная структура MAC-адресов
Standard MAC address structure

Последнее значение - число в шестнадцатеричном формате следующее после числа в MAC-адресе с наклейки
The last value is the number in hexadecimal format following the number in the MAC address from the sticker

Последнее значение - число в шестнадцатеричном формате следующее после числа в RF1 WLAN MAC
The last value is the number in hexadecimal format following the number in RF1 WLAN MAC

Последнее значение - число в шестнадцатеричном формате предшествующее числу в MAC-адресе с наклейки
The last value is the number in hexadecimal format preceding the number in the MAC address on the sticker

MAC-адрес с наклейки
MAC address from the sticker

Пример числового ряда в шестнадцатеричной системе счисления: .. AF B0 B1 B2 B3 B4 B5 B6 B7 B8 B9 BA BB BC BD BE BF C0 ..
Example of number series in the hexadecimal number system: .. AF B0 B1 B2 B3 B4 B5 B6 B7 B8 B9 BA BB BC BD BE BF C0 ..
------------------------------------------------------
Структура MAC-адресов в портированой прошивке Keenetic
MAC address structure in the ported Keenetic firmware

MAC-адрес с наклейки = RT6855/RT6856/MT7621 WAN MAC
MAC address from sticker = RT6855/RT6856/MT7621 WAN MAC

Последнее значение - число в шестнадцатеричном формате следующее после числа в MAC-адресе с наклейки (RT6855/RT6856/MT7621 WAN MAC = RF1 WLAN MAC)
The last value is the hexadecimal number following the MAC address on the sticker (RT6855/RT6856/MT7621 WAN MAC = RF1 WLAN MAC)

Последнее значение - число в шестнадцатеричном формате следующее после числа в RF1 MAC1
The last value is the number in hexadecimal format following the number in RF1 MAC1

Последнее значение - число в шестнадцатеричном формате предшествующее числу в MAC-адресе с наклейки
The last value is the number in hexadecimal format preceding the number in the MAC address on the sticker

MAC-адрес с наклейки = RF1 WLAN MAC
MAC address from the sticker = RF1 WLAN MAC

Пример числового ряда в шестнадцатеричной системе счисления: .. AF B0 B1 B2 B3 B4 B5 B6 B7 B8 B9 BA BB BC BD BE BF C0 ..
Example of number series in the hexadecimal number system: .. AF B0 B1 B2 B3 B4 B5 B6 B7 B8 B9 BA BB BC BD BE BF C0 ..

