
## Why

Aplikasi Android memiliki kemampuan untuk menulis informasi ke file log. Terkadang aplikasi mungkin menulis informasi sensitif ke file log yang dapat diakses oleh aplikasi lain di perangkat.

Sebagai bagian dari penilaian keamanan, penting bagi kami untuk mendapatkan log dan mengidentifikasi potensi masalah keamanan.

## What

Logcat adalah tool bawaan adb yang bisa digunakan untuk melihat log pesan sistem, termasuk pesan log yang ditulis oleh aplikasi yang sedang dijalankan.

## How

1. Run the following ADB command to print log messages to `stdout` as you browse through the target android application.
    
    ```
     $ adb logcat
    ```
    
2. Refer following link to see options that could be used with `adb logcat` command: [https://developer.android.com/studio/command-line/logcat](https://developer.android.com/studio/command-line/logcat)
    
3. As you browse the target application, check the logs to see if any sensitive information is being printed in plain text.
    
    ![Sensitive information in logs](https://null-android-pentesting.netlify.app/src/image/tools/4-adb-logcat.png)