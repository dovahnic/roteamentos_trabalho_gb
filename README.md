# roteamentos_trabalho_gb
Trabalho Grau B da cadeira de Roteamentos - UNISINOS 
### **TOPOLOGY OVERVIEW**


![image](https://user-images.githubusercontent.com/51249903/85484336-036a1c00-b59d-11ea-98bd-3dfb7dabc2c8.png)

### 
### **ROUTER CONFIGURATION ON NETWORK 1**

![image](https://user-images.githubusercontent.com/51249903/85484499-5348e300-b59d-11ea-981c-62e4ac0371fb.png)

**NETWORK AS 100**
_Protocol EIGRP_

**Router A:**

- _IP ADDRES - 192.168.10.0 - 192.168.0.0_

**COMMANDS:**

- enable
- config terminal
- route eigrp 100
-  network 192.168.10.0 
-  network 192.168.0.0


**Router B:**

- _IP ADDRES - 192.168.8.0 - 192.168.1.0 - 192.168.5.0_

**COMMANDS:**

- enable
- config terminal
- route eigrp 100
-  network 192.168.8.0 
-  network 192.168.1.0
-  network 192.168.5.0

**Router C**

- _IP ADDRES - 192.168.1.0 - 192.168.2.0_

**COMMANDS:**

- enable
- config terminal
- route eigrp 100
-  network 192.168.1.0 
-  network 192.168.2.0

**Router D**

- _IP ADDRES - 192.168.2.0 - 192.168.3.0_

**COMMANDS:**

- enable
- config terminal
- route eigrp 100
-  network 192.168.2.0 
-  network 192.168.3.0

**Router E** - Border

- _IP ADDRES - 192.168.3.0 - 192.168.30.0 - 192.168.4.0_

**COMMANDS:**

- enable
- config terminal
- route eigrp 100
-  network 192.168.3.0 
-  network 192.168.4.0
-  network 192.168.30.0

- exit
- route bgp 100
- neighbor 192.168.30.2 remote-as 200
- redistribute bgp 100


### **ROUTER CONFIGURATION ON NETWORK 2**

![image](https://user-images.githubusercontent.com/51249903/85485893-07e40400-b5a0-11ea-9b61-b698738a49cd.png)

**NETWORK AS 200**
_Protocol OSPF_

**Router G** - Border

- _IP ADDRES - 192.168.30.0 - 192.168.11.0 - 192.168.17.0_

**COMMANDS:**

- enable
- config terminal
- route ospf 1
-  network 192.168.11.0 255.255.255.0 area 0
-  network 192.168.17.0 255.255.255.0 area 0
- exit
- route bgp 200
- neighbor 192.168.30.1 remote-as 100
- redistribute bgp 200


**Router H**

- _IP ADDRES - 192.168.11.0 - 192.168.12.0_

**COMMANDS:**

- enable
- config terminal
- route ospf 1
-  network 192.168.11.0 255.255.255.0 area 0 
-  network 192.168.12.0 255.255.255.0 area 0

**Router I**

- _IP ADDRES - 192.168.12.0 - 192.168.13.0_

**COMMANDS:**

- enable
- config terminal
- route ospf 1
-  network 192.168.12.0 255.255.255.0 area 0 
-  network 192.168.13.0 255.255.255.0 area 0

**Router J**

- _IP ADDRES - 192.168.13.0 - 192.168.14.0_

**COMMANDS:**

- enable
- config terminal
- route ospf 1
-  network 192.168.13.0 255.255.255.0 area 0 
-  network 192.168.14.0 255.255.255.0 area 0

**Router K**

- _IP ADDRES - 192.168.14.0 - 192.168.20.0 - 192.168.15.0_

**COMMANDS:**

- enable
- config terminal
- route ospf 1
-  network 192.168.14.0 255.255.255.0 area 0 
-  network 192.168.15.0 255.255.255.0 area 0
-  network 192.168.20.0 255.255.255.0 area 0

**Router L**

- _IP ADDRES - 192.168.15.0 - 192.168.16.0_

**COMMANDS:**

- enable
- config terminal
- route ospf 1
-  network 192.168.15.0 255.255.255.0 area 0 
-  network 192.168.16.0 255.255.255.0 area 0

**Router M**

- _IP ADDRES - 192.168.16.0 - 192.168.17.0_

**COMMANDS:**

- enable
- config terminal
- route ospf 1
-  network 192.168.16.0 255.255.255.0 area 0 
-  network 192.168.17.0 255.255.255.0 area 0
