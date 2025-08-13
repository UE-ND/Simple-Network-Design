## Simple VLAN Network with SSH Management and more

## Topology  
Router (R1)
│
├── Switch1 (SW1)
│ ├── PC1 (VLAN 10)
│ ├── PC2 (VLAN 20)
│ └── PC3 (VLAN 30)
│
└── Switch2 (SW2)
 ├── PC4 (VLAN 10)
 ├── PC5 (VLAN 20)
 └── PC6 (VLAN 30)
 

## Key Features  
- **VLAN Segmentation**:  
  - VLAN 10: PC1 + PC4  
  - VLAN 20: PC2 + PC5  
  - VLAN 30: PC3 + PC6  
  - Native VLAN 99: Management  
- **Security**:  
  - SSH-only device access  
  - Privileged mode passwords  
  - Login banners  
- **Connectivity**:  
  - Inter-VLAN routing via router-on-a-stick  
  - Cross-switch VLAN communication  

## Verification Commands  
1. Check VLAN assignments:  SW1# show vlan brief
2. Verify trunk links:  SW1# show interfaces trunk
3. Test inter-VLAN connectivity:  SW1# ping <IP of another VLAN device>
4. Check SSH access:  SW1# ssh <IP of device>


## Security Notes  
- All device management requires SSH authentication  
- Native VLAN (99) isolates management traffic  
- Change default credentials in production environments  
- Use only on authorized networks  