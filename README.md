# OpenVPN3-Raspberry-Pi-5
Install of the openvpn3 package on a raspberry pi 5

1. Install nessesary packages
```bash
sudo apt-get install apt-transport-https curl -y
```
2. Retrieve the OpenVPN Inc package signing key
```
mkdir -p /etc/apt/keyrings
```
```
curl -sSfL https://packages.openvpn.net/packages-repo.gpg >/etc/apt/keyrings/openvpn.asc
```
3. Add source list
```
echo "deb [signed-by=/etc/apt/keyrings/openvpn.asc] https://packages.openvpn.net/openvpn3/debian bookworm main" \
 >> /etc/apt/sources.list.d/openvpn3.list
```
4. Update and Install
   
```
sudo apt-get update
```
```
sudo apt-get install openvpn3
```

> Finish
