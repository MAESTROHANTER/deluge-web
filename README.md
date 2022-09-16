# deluge-web
Step-by-step install

1. Update ubuntu packs
sudo apt-get update
sudo apt-get -y upgrade

2. Install deluge
sudo add-apt-repository ppa:deluge-team/stable
sudo apt-get update
sudo apt-get install deluged deluge-web deluge-console
nohup deluged &>/dev/null &
echo "username:password:10" >> ~/.config/deluge/auth
killall deluged
deluged
deluge-console "config -s allow_remote True"
deluge-web

Then connect to http://serverip:8112 and use first pass "deluge"

3. To start deluge service
deluged
deluge-web
