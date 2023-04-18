# ibm-project-submission-2019-batch-Ghanistkumar
ibm-project-submission-2019-batch-Ghanistkumar created by GitHub Classroom

Required Tools: snort, Pfsene, Virtual box

#Steps to instal and run snort on Ubuntu
sudo apt install snort

#after installation user need to do some configurations
change directory to /etc/snort/snort.conf

#in snort.conf file add your device ip into variabele HOME_NET
# value of DEBIAN_SNORT_HOME_NET s defined in the
ipvar HOME_NET 192.168.xx.x/24

#cd to /etc/snort/rules/local.rules to add your custom rules
alert icmp any any -> $HOME_NET any ( msg:"ICMP Ping Detected";  sid:19162101; rev:1;)

#to run the snort
sudo snort -q -l /var/log/snort -i enp1s0 -A console -c /etc/snort/snort.conf 

#after running the above command try to ping the device ip to see the result.








#refrences-------

#tool to create rules
http://www.cyb3rs3c.net/

