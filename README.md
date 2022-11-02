# cmpe283-assignment1
Discovering VMX Features

<h3>Work done by Srinishaa Prabhakaran</h3>

with machine configuration as : Machine type n2-standard-2 CPU platform Intel Cascade Lake Architecture x86/64

<b>Executed following commands on console</b><br><br> 
#gcloud compute instances export instance-10 --destination=cmpe283-1.yaml<br> --zone=us-central1-a<br> 

enabled virtualisation = true in cmpe283-1.yaml <br> 
advancedMachineFeatures: enableNestedVirtualization: true<br> <br> 

#gcloud compute instances update-from-file instance-10 --source=cmpe283-1.yaml --most-disruptive-allowed-action=RESTART --zone=us-central1-a<br> <br> 

Created folder :cmpe283-1<br> 
files created <br>
1. Make file <br>
2. cmpe283-1.c <br>
for IA32_VMX_PINBASED_CTLS 0x481 IA32_VMX_PROCBASED_CTLS 0x482 IA32_VMX_EXIT_CTLS 0x483 IA32_VMX_ENTRY_CTLS 0x484 <br>
IA32_VMX_PROCBASED_CTLS2 0x48B IA32_VMX_PROCBASED_CTLS3 0x492
<br>

Executed following commands: <br> 
#make sudo bash apt install gcc make <br> 
#exit<br> 
#sudo apt install linux-headers-$(uname -r) <br> 
#uname -r <br> 
#make<br> 
#sudo insmod ./cmpe283-1.ko<br> 
#sudo dmesg<br> 

Output Screenshots
![image](https://user-images.githubusercontent.com/111548210/199575911-aa6b9363-689c-4865-9ec8-2ba10595c9e8.png)
![image](https://user-images.githubusercontent.com/111548210/199574905-a8e6f00a-b02b-4af1-972e-cceccd4890d6.png)
![image](https://user-images.githubusercontent.com/111548210/199575971-cd3417c9-b81f-42f8-814b-17ebd934a79d.png)
