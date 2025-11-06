# wireguard_client

Role to connect a machine to a wireguard network.

## Requirements

Kernel which supports wireguard.

## Role Variables

```yaml
# Required variables
wireguard_client_iface_address: "" # Adresses of the wireguard machine
wireguard_client_private_key: "" # Private key of the machine
wireguard_client_public_key: "" # Public key of the machine
wireguard_client_endpoint: "" # Endpoint address of the wireguard server (e.g.: wg.example.com:51820)

# Optional variables
wireguard_client_allowed_ips: ""
wireguard_client_preshared_key: ""

# Defaults
wireguard_client_iface_name: wg0 # Name for the interface
wireguard_client_iface_mtu: 1300
wireguard_client_persistent_keep_alive: 15
```

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - {
            role: wittdennis.wireguard_client,
            wireguard_client_iface_address: 172.30.0.1/32,3d0d:3568:2136:c971:007f::1/128
            wireguard_client_private_key: <redacted>
            wireguard_client_public_key: <redacted>
            wireguard_client_endpoint: wg.example.com:51820
           }

## License

MIT
