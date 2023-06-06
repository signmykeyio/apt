# Signmykey APT repository

* Ensure you have curl and gpg
```
sudo apt update && sudo apt install ca-certificates curl gnupg
```
* Add Signmykey GPG to your APT truststore
```
curl https://gpg.signmykey.io/signmykey.pub | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/signmykey.gpg
```
* Add Signmykey repository
```
echo 'deb [signed-by=/etc/apt/trusted.gpg.d/signmykey.gpg] https://apt.signmykey.io stable main' | sudo tee /etc/apt/sources.list.d/signmykey.list
```
* Install Signmykey package
```
sudo apt update && sudo apt install signmykey
```