## Kết nối pi với wifi của bạn không cần dùng tới màn hình
* Rút thẻ nhớ cắm vào máy tính bất kì
* Tạo 1 file ssh trong thư mục boot
* Tạo file wpa_supplicant.conf:

    ```
    country=MY
    ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
    update_config=1

    network={
    ssid="SSID"
    psk="Password"
    key_mgmt=WPA-PSK
    }
    ```