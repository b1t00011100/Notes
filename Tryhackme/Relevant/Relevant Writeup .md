# Relevant Writeup

https://tryhackme.com/room/relevant?source=post_page-----a928d49becb4---------------------------------------

---

### RECONNAISSANCE

I performed a nmap scan on the target to identify open ports and services running on the target

`nmap -Pn -sC  -v <TARGET> -oA results`

`-Pn` : sending ping probes

`-sC` : Default script 

`-v` : verbose mode (maximum output)

`-oA` : output file 

  

![nmapres.png](Relevant%20Writeup/nmapres.png)

### FOOTHOLD

Checked out the webpage, it was a IIS landing page

![webpage.png](Relevant%20Writeup/webpage.png)

Since nothing interesting was found on the HTTP pages, moved to **smb enumeration** and found an interesting share

![smbrecon.png](Relevant%20Writeup/smbrecon.png)

I connected to the share and found a password file :

![smbext.png](Relevant%20Writeup/smbext.png)

Transferred it to my local machine, and when opened it had creds but they were in `base64` encoded format.

![base64dec.png](Relevant%20Writeup/base64dec.png)

Decoded them using :

`echo <encoded-string> | base64 -d`

So a natural instinct after finding out these creds was to use them to login to `rdp`,  but it failed, then after some r&d found this `CVE` :

[NVD - cve-2017-0143](https://nvd.nist.gov/vuln/detail/cve-2017-0143)

The vulnerability lead to a remote code exec, so to exploit it, created an `.aspx` payload using `msfvenom`.

 

![msfvenom.png](Relevant%20Writeup/msfvenom.png)

Then uploaded the payload on the smb server, using `put <file_name>` .

Did some research and found that sometimes smb shares are hosted on the webservers. tried on both the servers running and succeeded on the one running on **port 49663.**

Then started a netcat listener and executed the payload through **http** to get a reverse shell.

![runexp.png](Relevant%20Writeup/runexp.png)

![shell.png](Relevant%20Writeup/shell.png)

With shell access, was able to capture the `user_flag` from Bob’s Desktop

![userflagblackedout.png](Relevant%20Writeup/userflagblackedout.png)

### PRIVILEGE ESCALATION

I am not that familiar with windows hacking, so this was difficult for me so just did the basic methodology of Linux privilege escalation by checking out privlieges.

![checkingpriv.png](Relevant%20Writeup/checkingpriv.png)

and `SeImpersonatePrivilege` seemed interesting so did some research and found out theis privilege enabled could potentially escalate to admin using dirty potato or spoolspoof exploits. I then used the printspoofer’s exploit which is available on his github :

https://github.com/itm4n/PrintSpoofer/releases

The transferred the exploit from my local machine to the target

First had to spawn a Powershell to do this step : `powershell -ep bypass`

![localtransf.png](Relevant%20Writeup/localtransf.png)

Then ran the exploit.

![runningthescript.png](Relevant%20Writeup/runningthescript.png)

Got the admin shell then went to `C:\Users\Administrator\Desktop`  for the `root_flag`.

![rootflag.png](Relevant%20Writeup/rootflag.png)

DONE.
