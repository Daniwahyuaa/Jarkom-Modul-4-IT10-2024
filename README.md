# Jarkom-Modul-4-IT10-2024

## Anggota Team:

| Nama | NRP                    |
|---------------|---------------------------------|
| Dani Wahyu Anak Ary    | 5027231038 |
| Abid Ubaidillah A      | 5027231089 |

### Topologi GNS3
![image](https://github.com/user-attachments/assets/e650aa66-8c84-4796-9493-b064c9d786dc)

### Topologi CPT
![Topologi CPT](https://github.com/user-attachments/assets/7521821a-0ad4-40c3-af49-e2f7a3ad84fa)

### Subnetting dan Pengelompokkan
- Pembagian Rute:
  ![image](https://github.com/user-attachments/assets/09399db1-95ac-4536-9c0c-11830ed39cbb)

- Subnetting
  ![Pengelompokan Subnetting](https://github.com/user-attachments/assets/558bf6d5-de2e-496a-9874-cb1806676d34)

- Pengelompokkan 1

  ![image](https://github.com/user-attachments/assets/01a11512-d0a2-4d03-af2d-a6abfb79b9de)
  ![Pembagian-1](https://github.com/user-attachments/assets/5695c158-14cd-45d3-abad-52db8028a3dd)

- Pengelompokkan 2

  ![image](https://github.com/user-attachments/assets/6b2ebed9-9d64-4c21-aecb-875a23b3d161)
  ![Pembagian-2](https://github.com/user-attachments/assets/abf7f9db-a2b8-4d04-a52b-958c74e4ea8f)

- Pengelompokkan 3

  ![image](https://github.com/user-attachments/assets/b834129d-4546-4d25-81b3-547aa4b65383)
  ![Pembagian-3](https://github.com/user-attachments/assets/1e0d9f15-a8f3-4fb5-be28-14d3e23b8bad)

- Pembagian 4
  
  ![image](https://github.com/user-attachments/assets/d30ce302-5dae-479c-9074-7c39ede1eef2)
  ![image](https://github.com/user-attachments/assets/099dd920-5246-4a30-9899-08aec915c2c1)


- Pembagian 5
  
  ![image](https://github.com/user-attachments/assets/a4f75739-2ca5-494f-95cb-e39017659b84)
  ![Pembagian-4](https://github.com/user-attachments/assets/ab9b26d7-16b1-4637-a909-cf1cfba522cc)

- Pembagian 6

  ![image](https://github.com/user-attachments/assets/90171371-be9e-40d8-9012-71c12ed5d53e)
  ![Pembagian-5](https://github.com/user-attachments/assets/e4a06189-c9ba-40d7-9d7a-10b5ec9379b8)

- Pembagian 7
  
  ![image](https://github.com/user-attachments/assets/319ef080-4820-4343-88bb-a06896f1b7a5)
  ![Pembagian-7](https://github.com/user-attachments/assets/78991150-d070-44c0-91f2-7d690dcbc736)

- Pembagian 8

  ![image](https://github.com/user-attachments/assets/7da3456e-e997-4499-99c7-ad5495bca136)
  ![Pembagian-8](https://github.com/user-attachments/assets/32b85742-d208-4097-9b13-fd9a97011ff9)

### Tree 
Setelah dilakukan pengelompokan IP, kita melakukan pembagian IP menggunakan tree untuk kelompok yang telah dibagikan sebelumnya dengan hasil seperti berikut!

![image](https://github.com/user-attachments/assets/411564e8-bd90-43c2-823f-aead032b2ced)

### Configurasi
#### Hololive (GateAway)
```
#A15
bash
auto eth1
iface eth1 inet static
    address 192.238.66.5
    netmask 255.255.255.252

#A16
auto eth2
iface eth2 inet static
    address 192.238.4.5
    netmask 255.255.255.252

#A21
auto eth3
iface eth3 inet static
    address 192.238.10.25
    netmask 255.255.255.252
```
#### Holo-EN (Gateway)
```
#A15
auto eth0
iface eth0 inet static
    address 192.238.66.6
    netmask 255.255.255.252
    gateway 192.242.66.5

#A14
auto eth1
iface eth1 inet static
    address 192.238.66.1
    netmask 255.255.255.252

#A20
auto eth2
iface eth2 inet static
    address 192.238.16.33
    netmask 255.255.255.252
```
#### Holo-Myth (GateAway)
```
#A14
auto eth0
iface eth0 inet static
    address 192.238.66.2
    netmask 255.255.255.252
    gateway 192.242.66.1

#A11
auto eth1
iface eth1 inet static
    address 192.238.64.1
    netmask 255.255.254.0

#A12
auto eth2
iface eth2 inet static
    address 192.238.32.65
    netmask 255.255.255.248
```
#### Gura_Ame_Ina (Client)
```
#A11
auto eth0
iface eth0 inet static
    address 192.238.64.2
    netmask 255.255.254.0
    gateway 192.238.64.1

Kiara_Calli (Client)
#A11
auto eth0
iface eth0 inet static
    address 192.238.64.3
    netmask 255.255.254.0
    gateway 192.238.64.1
\\
```
#### Holo Advent (Gateway)
```
#A20
auto eth0
iface eth0 inet static
    address 192.238.16.34
    netmask 255.255.255.252
    gateway 192.238.16.33

#A8
auto eth1
iface eth1 inet static
    address 192.238.16.1
    netmask 255.255.255.224
```
#### FuwaMoco (Client)
```
#A8
auto eth0
iface eth0 inet static
    address 192.238.16.2
    netmask 255.255.255.224
    gateway 192.238.16.1
```
#### Shiori_Nerissa (Client)
```
#A8
auto eth0
iface eth0 inet static
    address 192.238.16.3
    netmask 255.255.255.224
    gateway 192.238.16.1
```
#### Biboo (Client
```
#A8
auto eth0
iface eth0 inet static
    address 192.238.16.4
    netmask 255.255.255.224
    gateway 192.238.16.1
```
#### Project-Hope (Gateway)
```
#A12
auto eth0
iface eth0 inet static
    address 192.238.32.66
    netmask 255.255.255.248
    gateway 192.238.32.65

#A10
auto eth1
iface eth1 inet static
    address 192.238.32.73
    netmask 255.255.255.248
```
#### Irys (Client)
```
#A10
auto eth0
iface eth0 inet static
    address 192.238.32.74
    netmask 255.255.255.248
    gateway 192.238.32.73
```
#### Holo-Council (Gateway)
```
#A12
auto eth0
iface eth0 inet static
    address 192.238.32.67
    netmask 255.255.255.248
    gateway 192.238.32.65

#A9
auto eth1
iface eth1 inet static
    address 192.238.32.1
    netmask 255.255.255.192
```
#### Kronii_Mumei (Client)
```
#A9
auto eth0
iface eth0 inet static
    address 192.238.32.2
    netmask 255.255.255.192
    gateway 192.238.32.1
```
#### Bae_Fauna (Client)
```
#A9
auto eth0
iface eth0 inet static
    address 192.238.32.3
    netmask 255.255.255.192
    gateway 192.238.32.1
```
#### Holo-ID (Gateway)
```
#A16
auto eth0
iface eth0 inet static
    address 192.238.4.6
    netmask 255.255.255.252

#A17
auto eth1
iface eth1 inet static
    address 192.238.4.1
    netmask 255.255.255.252

#A18
auto eth2
iface eth2 inet static
    address 192.238.16.65
    netmask 255.255.255.252

#A19
auto eth3
iface eth3 inet static
    address 192.238.34.1
    netmask 255.255.255.252
```
#### AREA15 (Gateway)
```
#A17
auto eth0
iface eth0 inet static
    address 192.238.4.2
    netmask 255.255.255.252
    gateway 192.238.4.1
#A1
auto eth1
iface eth1 inet static
    address 192.238.0.1
    netmask 255.255.252.0
```
#### lofi (Client)
```
#A1
auto eth0
iface eth0 inet static
    address 192.238.0.2
    netmask 255.255.252.0
    gateway 192.238.0.1
```
#### Moona (Client)
```
#A1
auto eth0
iface eth0 inet static
    address 192.238.0.3
    netmask 255.255.252.0
    gateway 192.238.0.1
```
#### Risu (Client)
```
#A1
auto eth0
iface eth0 inet static
    address 192.238.0.4
    netmask 255.255.252.0
    gateway 192.238.0.1
```
#### holoro (Gateway)
```
#A18
auto eth0
iface eth0 inet static
    address 192.238.16.66
    netmask 255.255.255.252
    gateway 192.238.16.65

### A2
auto eth1
iface eth1 inet static
    address 192.238.16.1
    netmask 255.255.252.192
```
#### Ollie (Client)
```
#A2
auto eth0
iface eth0 inet static
    address 192.238.16.2
    netmask 255.255.252.192
    gateway 192.238.16.1
```
#### Anya (Client)
```
#A2
auto eth0
iface eth0 inet static
    address 192.238.16.3
    netmask 255.255.252.192
    gateway 192.238.16.1
```
#### Reine (Client)
```
#A2
auto eth0
iface eth0 inet static
    address 192.238.16.4
    netmask 255.255.252.192
    gateway 192.238.16.1
```
#### holoh3ro (Gateway)
```
#A19
auto eth0
iface eth0 inet static
    address 192.238.34.2
    netmask 255.255.255.252
    gateway 192.238.34.1
```
