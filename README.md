# Cottage Network
## Components
**ISP Modem / Router**:  
Calix 844 G  
Has 4 Gbit ethernet ports

**10Gtek Gigabit Ethernet Media Converter with GBIC**:  
[https://www.amazon.ca/Ethernet-Converter-SFP-1000Base-Tx-Transceiver/dp/B06XBSZJL3](https://www.amazon.ca/Ethernet-Converter-SFP-1000Base-Tx-Transceiver/dp/B06XBSZJL3)  
Will go with this option as it's cheaper than a Ubiquiti switch or Dream Machine Pro

**Conduit**:  
100ft of old PVC mainline water tubing  
1/2" or 3/4" inner diameter. Need to confirm.

**3M Wire Pulling Lubricant**  
[https://www.amazon.ca/dp/B001AO3FHK/?coliid=IZW33GIBQRD4C&colid=2KYNMYSP4GZA&psc=1](https://www.amazon.ca/dp/B001AO3FHK/?coliid=IZW33GIBQRD4C&colid=2KYNMYSP4GZA&psc=1)
Not sure if this is necessary but don't want to damage fibre

**40m / 130ft of LC/LC Multi-mode fibre - Monoprice**:  
[https://www.monoprice.com/product?p_id=2616](https://www.monoprice.com/product?p_id=2616)  
Product is OM1. Not sure which OM matters or is appropriate

**Cottage 2 Switch**:  
Ubiquiti US-8-150W  
[https://ca.store.ui.com/products/unifi-switch-8-150w?_pos=1&_sid=2d54543af&_ss=r](https://ca.store.ui.com/products/unifi-switch-8-150w?_pos=1&_sid=2d54543af&_ss=r)  
Has POE and SFP port

**Mini GBIC for Cottage 2 Switch**
10GTek 1000BASE-SX  
[https://www.amazon.ca/10Gtek-GLC-SX-MMD-GLC-SX-MM-Transceiver-1000Base-SX/dp/B01CN82KQI/](https://www.amazon.ca/10Gtek-GLC-SX-MMD-GLC-SX-MM-Transceiver-1000Base-SX/dp/B01CN82KQI/)  
SFP Module to connect to cottage 1


**Cottage 2 Access Point / WiFi**  
Ubiquiti FlexHD  
[https://ca.store.ui.com/collections/unifi-network-wireless/products/unifi-flexhd](https://ca.store.ui.com/collections/unifi-network-wireless/products/unifi-flexhd)

## Topology
```
 +--------------------------------------------------+                                          
 |           |                                      |                                          
 |           | ISP Fibre Feed (Internet)            |                                          
 |           | 2Gbps / 1Gbps                        |                                          
 |           |                                      |                                          
 | +------------------+           +-------------+   |                                          
 | |                  |           |             |   |                                          
 | |    Calix 844G    |-----------|   10GTek    |   |                                          
 | |                  |   Cat6A   |             |   |                                          
 | +------------------+           +------------++   |                                          
 |                                |SFP Port    |    |                                          
 |                                |1000Base-SX |    |                                          
 |                                |Module      |    |                                          
 |                                +------------+    |                                          
 |                                         |        |                                          
 +-----------------------------------------|--------+                                          
  Cottage 1                                |                                                   
                                           |                                                   
                                           |                                                   
                                           |                                                   
                                           | Multi-mode LC/LC Fibre                            
                                           |                                                   
                                           |                                                   
  Cottage 2                                |                                                   
 +--------------------------------------------------+                                          
 |  +--------+                             |        |                                          
 |  |        |                     +------------+   |                                          
 |  |AP      |                     |SFP Port    |   |                                          
 |  |Ubiquiti|                     |1000BASE-SX |   |                                          
 |  |FlexHD  |                     |Module      |   |                                          
 |  |        |                 +---+------------+-+ |                                          
 |  |        -------------------                  | |                                          
 |  |        |    POE Cat6A    |Ubiquiti US-8-150W| |                                          
 |  |        |                 |                  | |                                          
 |  |        |                 +------------------+ |                                          
 |  +--------+                                      |                                          
 +--------------------------------------------------+ 
```
#Questions and Comments

* Do I need a pull tape or can I just use a pull string with a vaccum to get it down the hose? Seems like a much cheaper solution for something I'm only doing once. See [https://www.youtube.com/watch?v=jo3dmunFodE&list=PL8ln136hCxIhsyC5WTF774vlB864leBwu&index=3](https://www.youtube.com/watch?v=jo3dmunFodE&list=PL8ln136hCxIhsyC5WTF774vlB864leBwu&index=3)
* Need to measure width of a dual LC fibre connector to see if it fits through the conduit. If I separate. I need to figure out how to bend the separate cables to pull without breaking them

