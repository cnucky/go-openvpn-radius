### Go-OpenVPN-Radius

As basic go app that can be used by applications such as OpenVPN to forward radius requests, see releases for prebuilt binaries, add the following to your openvpn server.conf:

```
script-security 2
tmp-dir /dev/shm
auth-user-pass-verify "go-openvpn-radius -secret '{{openvpn_radius_secret}}' -server {{openvpn_radius_address}} -file" via-file
```