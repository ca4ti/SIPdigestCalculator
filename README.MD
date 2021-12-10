SIPdigestcalculator.exe -u username -r realm -p password -n nonce -uri SIP URI
or
SIPdigestcalculator.exe -u username -r realm -p password -n nonce -cn client nonce -nc nonce count -uri SIP URI


wget https://raw.githubusercontent.com/OlegPowerC/SIPdigestCalculator/master/SIPdigestcalculator.go
wget https://golang.org/dl/go1.17.linux-amd64.tar.gz
sudo tar -zxvf go1.17.linux-amd64.tar.gz -C /usr/local/
echo "export PATH=/usr/local/go/bin:${PATH}" | sudo tee /etc/profile.d/go.sh
source /etc/profile.d/go.sh
echo "export PATH=/usr/local/go/bin:${PATH}" | sudo tee -a $HOME/.profile
source $HOME/.profile
go version

SIPdigestcalculator -u username -r realm -p password -n nonce -uri SIP URI 
or 
SIPdigestcalculator -u username -r realm -p password -n nonce -cn client nonce -nc nonce count -uri SIP URI

go run SIPdigestcalculator.go -u 986516203 -r asterisk -p 986516203 -n 1639147959/f3cfe57e08a8e43025d13172e1ab3046 -uri sip:10.1.1.215  -cn b0cb70bfd4c64b8db244419f9b20c58b -nc 00000001 
