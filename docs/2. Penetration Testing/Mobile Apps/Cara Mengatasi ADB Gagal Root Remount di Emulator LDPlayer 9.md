
Ketika saya ingin melakukan instalasi ssl cert burpsuite pada emulator android ldplayer9 muncul pesan kesalahan gagal remount dikarenakan permission denied. Saya menemukan solusi pada artikel dengan cara melakukan enabled pada settingan ldplayer.


```sh
C:\Program\leidian\LDPlayer9> adb remount
remount of the / superblock failed: Permission denied
remount failed
```

![](https://i.imgur.com/kmAVPD7.png)

Setelah itu coba lakukan adb remount ulang. maka akan berhasil dan bisa dilakukan instalasi ssl cert dari burpsuite.


```sh
C:\Program\leidian\LDPlayer9> adb remount
remount succeded
```


##### Sumber : [https://blog.csdn.net/qq_50969362/article/details/134044269](https://blog.csdn.net/qq_50969362/article/details/134044269)