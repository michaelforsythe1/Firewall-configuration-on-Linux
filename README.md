<h1>Linux Firewall configuration</h1>

<h2>Description</h2>
Firewalls are crucial for protecting networks from unauthorized access and potential threats. In this lab, I will be configuring a firewall on an Ubuntu system using UFW (Uncomplicated Firewall). 
<br />


<h2>Prerequisites</h2>

- *Basic knowledge of Linux commands*
- *Zorin OS (virtual machine)*


<h2>Project walkthrough</h2>

<br/> Assuming that Zorin OS (an Ubuntu system has been installed), first update the system <br/>
 <br/>
<img src="https://i.postimg.cc/0jxXNn8G/Screenshot-2024-07-28-151138.png" height="60%" width="60%" alt="update system"/>
<br />
 <br/> Install UFW and enable it <br/>
 <br/>
<img src="https://i.postimg.cc/tJZJY32T/Screenshot-2024-07-28-151432.png" height="60%" width="60%" alt="Enable UFW"/>
<br />
<br />
Allow SSH connections to prevent locking myself out of the system  <br/>
 <br/>
<img src="https://i.postimg.cc/28YVcZhv/Screenshot-2024-07-28-151546.png" height="60%" width="60%" alt="Update system"/>
<br />
<br />
Alternatively, the port number can be used in the command, instead of the name, like this *'sudo ufw allow 22/tcp'*  <br/>
 <br/>
<img src="https://i.postimg.cc/QdH91rcn/Screenshot-2024-07-28-152024.png" height="60%" width="60%" alt="Alt port number"/>
<br />
<br />
Continue by allowing specific services like http, https, and a range of ports  <br/>
 <br/>
<img src="https://i.postimg.cc/3Rk5KnG6/Screenshot-2024-07-28-152620.png" height="60%" width="60%" alt="allow ports"/>
<br />
<br />
Allow specific ip addresses and its subnet <br />
<img src="https://i.postimg.cc/ZnHZDqbr/Screenshot-2024-07-28-153832.png" height="60%" width="60%" alt="allow IP and subnet"/>
<br />
<br />
Deny port 23 and a specific IP address <br />
 <br/>
<img src="https://i.postimg.cc/c4yMZhtb/Screenshot-2024-07-28-154130.png" height="60%" width="60%" alt="Deny ports"/>
<br />
<br />
Summary of configured rules  <br />
 <br/>
<img src="https://i.postimg.cc/hP14v4hq/Screenshot-2024-07-28-154251.png" height="60%" width="60%" alt="summary of rules"/>
<br />
<br />
Alternatively, the summary of configured rules can be viewed in numbered mode using the command *sudo ufw status numbered*. From here, we can easily delete a rule by specifying the rule number, *e.g. 'sudo ufw delete 2'*  <br/>
 <br/>
<img src="https://i.postimg.cc/Yqjqy1F0/Screenshot-2024-07-28-154401.png" height="60%" width="60%" alt="specifying rule number"/>
<br />
<br />
Using rule specification  <br/>
 <br/>
<img src="https://i.postimg.cc/pdhpmNgY/Screenshot-2024-07-28-154608.png" height="60%" width="60%" alt="rule specs"/>
<br />
<br />
Time to test the firewall rules from another system (Another VM hosting Linux Mint with the 'nmap' utility installed). 
NMAP (network mapper) is used for network discovery and security auditing  <br/>
<br/>
<img src="https://i.postimg.cc/sD5P2Nkh/Screenshot-2024-07-28-235330.png" height="80%" width="80%" alt="Test rules"/>
<br />

