# How to Install Grafana in Raspberry PI

- Add the Grafana packages to apt
```bash
$ wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -
$ echo "deb https://packages.grafana.com/oss/deb stable main" | sudo tee /etc/apt/sources.list.d/grafana.list
```
- Update and install the binaries
```bash
$ sudo apt update && sudo apt install -y grafana
```
- Enable the service and set to run at boot
```bash
$ sudo systemctl unmask grafana-server.service
$ sudo systemctl start grafana-server
$ sudo systemctl enable grafana-server.service
```
