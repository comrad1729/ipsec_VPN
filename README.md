# Site-to-Site IPsec VPN Lab | GNS3

## Project Overview

This project demonstrates the configuration, implementation, and troubleshooting of a Site-to-Site IPsec VPN using GNS3.

The objective is to establish secure communication between two geographically separated networks through an encrypted IPsec tunnel.

The lab covers IKE negotiation, IPsec Phase 1 and Phase 2, pre-shared key authentication, encryption, routing, and packet-level analysis using Wireshark.

## Objectives

- Configure Site-to-Site IPsec VPN connectivity.
- Understand IKE Phase 1 and Phase 2 negotiations.
- Configure encryption and authentication parameters.
- Establish encrypted communication between two LAN networks.
- Analyze IKE and ESP packets using Wireshark.
- Understand VPN troubleshooting and verification.

## Lab Environment

| Component | Technology |
|---|---|
| Network Simulator | GNS3 |
| VPN Technology | IPsec |
| IKE | IKEv1 |
| Authentication | Pre-Shared Key |
| Encryption | As configured in lab |
| Packet Analysis | Wireshark |
| Network Devices | Cisco Routers |

## Network Topology

Add your GNS3 topology screenshot here.

## VPN Architecture

The VPN connection involves two major negotiation phases:

### Phase 1 – IKE Negotiation

Establishes a secure management channel between VPN peers.

Parameters include:
- Encryption algorithm
- Authentication method
- Hash/integrity algorithm
- Diffie-Hellman group
- Pre-shared key
- IKE lifetime

### Phase 2 – IPsec Negotiation

Establishes the IPsec Security Associations used to protect actual data traffic.

Parameters include:
- ESP encryption
- Integrity algorithm
- PFS
- IPsec lifetime
- Local and remote traffic selectors

## Configuration

The lab includes:
- Interface and IP addressing
- Routing configuration
- IKE Phase 1 policy
- Pre-shared key authentication
- IPsec transform set
- Crypto ACL / traffic selectors
- Crypto map configuration
- Application traffic testing

Refer to the Configurations folder for device configurations.

## Verification

The following commands are used to verify VPN establishment:

```bash
show crypto isakmp sa
show crypto ipsec sa
show crypto session detail
show crypto map
show ip route
```

## Wireshark Packet Analysis

Packet captures are included to demonstrate:

- IKE Phase 1 negotiation
- IKE Quick Mode negotiation
- UDP 500 and UDP 4500 traffic
- ESP encrypted packets
- Encrypted communication between VPN peers

## Troubleshooting Scenarios

The lab can be used to understand and simulate:

1. Incorrect pre-shared key.
2. IKE Phase 1 proposal mismatch.
3. IPsec Phase 2 proposal mismatch.
4. Proxy ID / traffic selector mismatch.
5. Incorrect routing.
6. NAT-related VPN connectivity issues.

## Key Learnings

- Understanding of IKE and IPsec negotiation.
- Practical site-to-site VPN configuration.
- VPN Security Association verification.
- Wireshark packet inspection.
- VPN troubleshooting methodology.

## Disclaimer

This is a self-created educational lab built in GNS3 for networking and network security learning. It is not a production deployment.

No real production credentials or sensitive network information are included.
