# breed-mt7621-pbr-m1.bin
PandoraBox PBR-M1 dedicated, DDR3 memory suitable, default 512MB DDR AC timing parameters, baud rate 115200, reset button GPIO#18
* Xiaodu Router (Ai-BR100)
* Phicomm FIR300M/302M
* ASUS RT-N14U
* HiWiFi Routers 1S/2/3 (HC5661/HC5761/HC5861)
* Netcore NO1
* Buffalo WHR-1166DHP
* Youku Router-Bao YK1
* iKuai
* RippleOS
* TOTOLINK A3004NS
* Netgear WNDR3700 v5
* JDCloud-1 (JD_RE_SP_01B) Router
*	etc.

<p align="center">
<a href="#"><img src="/breed-mt7621-pbr-m1 1.1 R1338/Screenshots/01%20breed-mt7621-pbr-m1-%5BR1338%5D.png" width="800"</a>

## 1. Binwalk  
`binwalk breed-mt7621-xiaomi-r3g.bin                                                               `  
`                                                                                                  `  
`DECIMAL  HEXADECIMAL  DESCRIPTION                                                                 `  
`--------------------------------------------------------------------------------------------------`  
`513   0x1D59  JBOOT STAG header, image id: 7, timestamp 0x5004418, image size: 1074814976 bytes,  `  
`              image JBOOT checksum: 0x218, header JBOOT checksum: 0x2100                            `  
`0520  0x2918  Copyright string: "Copyright (C) 2021 HackPascal <hackpascal@gmail.com>"            `  
`3384  0x5B58  LZMA compressed data, properties: 0x6D, dictionary size: 33554432 bytes,            `  
`              uncompressed size: 285143 bytes                                                       `

## 2. Split
`dd if=breed-mt7621-pbr-m1-R1338.bin of=01Boot-pbr-m1-R1338 bs=1 count=23384`  
`dd if=breed-mt7621-pbr-m1-R1338.bin of=02Packed_Data-pbr-m1-R1338-Cn.lzma bs=1 skip=23384`

## 3. LzmaInfo
`lzmainfo 02Packed_Data-pbr-m1-R1338-Cn.lzma`  
`Uncompressed size:             0 MB (285143 bytes)`  
`Dictionary size:               32 MB (2^25 bytes)`  
`Literal context bits (lc):     1`  
`Literal pos bits (lp):         2`  
`Number of pos bits (pb):       2`

## 4. Unpack
`lzma462 d 02Packed_Data-pbr-m1-R1338-Cn.lzma 02Data-pbr-m1-R1338-Cn`

## 5. Перевести китайскую грамоту на более понятную в 010 Editor
В процессе перевода следим за размер файла 02Data-pbr-m1-R1338-En - 285143 байт, размер должен остаться неизменным!!!

## 6. Pack - использовать lzma462.exe он выдает идентичный оригинальному Breed размер архива
`lzma462 e 02Data-pbr-m1-R1338-En 02Packed_Data-pbr-m1-R1338-En.lzma -d25 -lc1 -lp2 -pb2`

## 7. Сборка переведенного Breed
`copy /b 01Boot-pbr-m1-R1338 + 02Packed_Data-pbr-m1-R1338-En.lzma breed-mt7621-pbr-m1-En.bin`

## 8. Patch
Для информации.  Размер 02Data-pbr-m1-R1338-Cn.lzma - `81702` байт = `00 01 3F 26` (Hex)
  
a) Перевести размер 02Data-pbr-m1-R1338-En.lzma из десятичного формата в шестнадцатеричный  
Размер 02Data-pbr-m1-R1338-En.lzma - `81287` байт = `00 01 3D 87` (Hex)
  
b) Пропатчить 4 байта в итоговом, переведенном breed-mt7621-pbr-m1-En.bin начиная со смещения `0x000000005B4C` до `0x000000005B4F`
