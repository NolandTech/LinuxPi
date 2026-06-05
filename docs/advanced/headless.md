#### **Enable SSH:**
In the boot directory create file called "ssh"(no extention)

#### **Setup Wifi credentials:** 
In the boot directory create file called "wpa_supplicant.conf" and Add:

```shell
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1
country=CA

network={
        ssid="Networkname"
        psk="Network Password"
}
```

#### **Set static IP:**
in the boot/etc/ directory create file called "dhcpcd.conf" and Add: 

```shell
interface wlan0
static ip_address=192.168.0.XXX
static routers=192.168.0.1
static domain_name_servers=192.168.0.1 8.8.8.8
```