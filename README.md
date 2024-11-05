# custom-apt-repo

This is a custom test repository.
Following steps can be performed to download the package from this repository using apt.

```
sudo mkdir -p /etc/apt/keyrings/
curl https://p919h.github.io/custom-apt-repo/dummy-public-key.gpg | sudo gpg --dearmor -o /etc/apt/keyrings/abcorp-abperf-repo.gpg
echo "deb [arch=amd64  signed-by=/etc/apt/keyrings/abcorp-abperf-repo.gpg] https://p919h.github.io/custom-apt-repo/custor-repo ./stable main" | sudo tee /etc/apt/sources.list.d/abcorp-abperf.list
sudo apt update
sudo apt install abperf
```
