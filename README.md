# SP-Style
This repositiry describes how to configure a SP Style DC with multiple VRFs and MAC-VRFs 

Here is the topology of the lab :

<img width="548" alt="image" src="https://github.com/lazabou/SP-Style/assets/10668741/18a03a18-12d3-490e-b486-4831dcd299aa">

Add a tag "spine" to the Spine devices 

<img width="662" alt="image" src="https://github.com/lazabou/SP-Style/assets/10668741/8955dc0f-c099-4c5c-b9a9-c08b32220b65">

Create the following resource pools :
![image](https://github.com/lazabou/SP-Style/assets/10668741/47e43a4b-7e56-4461-adb5-82bf7036676b)

Create the following resource generators : 
- ASN per internal device (leaves and spines)
- LACP id per generic system
- IP addresses for internal links (between leaves and spines)
- Loopback IP per internal device (leaves and spines)
![image](https://github.com/lazabou/SP-Style/assets/10668741/0b31e609-d6a2-4eaf-b30c-2bc9c25b2634)

The tenants are defined like this in a menu called Tenants :
- an integer called RT-RD (unique value automatically generated from a pool)
- the list of VLANs with a name and a vlan-id (the type is VLAN)
- if the VLAN is L3, define a Host IPv4 that has the same name as the VLAN 
![image](https://github.com/lazabou/SP-Style/assets/10668741/38ca39cb-2fab-42f5-b688-e7afd12a9d48)






