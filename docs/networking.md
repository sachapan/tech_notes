## Network notes

### Private address ranges

| RFC 1918 name | IP address range | Number of addresses | Largest CIDR block | Host ID size | Mask bits | description |
| -- | -- | -- | -- | -- | -- | -- |
| 24 bit block | 10.0.0.0-10.255.255.255 | 16,777,216 | 10.0.0.8/8 255.0.0.0 | 24 bits | 8 bits | single class A network |
| 20 bit block | 176.16.0.0-172.31.255.255 | 1,048,576 | 176.16.0.0/12 255.240.0.0 | 20 bits | 12 bits | 16 contiguous class B networks |
| 16 bit block | 192.168.0.0-192.168.255.255 | 65,536 | 192.168.0.0/16 255.255.0.0 | 16 bits | 16 bits | 256 contiguous class C networks|

### network testing

#### speedtest

- [without the cruft](https://librespeed.org/)

#### TLS 

- Test certificate chain
  `openssl\ s_client\ -showcerts\ -connect google.com:443`

