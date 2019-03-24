For Ubuntu 14.04 and 16.04
sudo apt-get install software-properties-common -y
sudo add-apt-repository ppa:max-c-lv/shadowsocks-libev -y
sudo apt-get update
sudo apt install shadowsocks-libev

Ubuntu 16.10 or higher
sudo apt update
sudo apt install shadowsocks-libev

sudo vim /etc/shadowsocks-libev/config.json

{
    "server":["[::0]", "0.0.0.0"],
    "server_port":443,
    "local_port":1080,
    "password":"pw",
    "timeout":60,
    "method":"chacha20-ietf-poly1305"
}

sudo systemctl start shadowsocks-libev
