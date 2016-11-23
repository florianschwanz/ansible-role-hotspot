# Ansible Role: Hotspot

Sets up a hotspot on a Raspberry Pi.

## Requirements

None.

## Role Variables

    interfaces_config_file: '/etc/network/interfaces'

Interfaces configuration file.

    hostapd_default_file: '/etc/default/hostapd'

hostapd default file.

    hostapd_config_file: '/etc/hostapd/hostapd.conf'

hostapd configuration file.

    dnsmasq_conf_file: '/etc/dnsmasq.conf'

dnsmasq configuration file.

    sysctl_conf_file: '/etc/sysctl.conf'

sysctl configuration file.

    accesspoint_file: '/etc/network/if-up.d/accesspoint'

Accesspoint file.

    hostapd_interface: 'wlan0'

Interface name:

    hostapd_driver: 'nl80211'

Used wifi driver.

    hostapd_ctrl_interface: '/var/run/hostapd'

    hostapd_ctrl_interface_group: '0'

    hostapd_ssid: 'RaspberryPi'

SSID of the created wifi network.

    hostapd_passphrase: ''

Password of the created wifi network.

    hostapd_channel: '1'

    hostapd_hw_mode: 'g'

    hostapd_ieee80211n: '1'

    hostapd_wpa: '2'

    hostapd_wpa_key_mgmt: 'WPA-PSK'

    hostapd_wpa_pairwise: 'CCMP'

    hostapd_rsn_pairwise: 'CCMP'

    hostapd_country_code: 'DE'

## Dependencies

None.

## Example Playbook

    - hosts: all
      roles:
        - { role: interoberlin.hotspot, hostapd_passphrase: mypassword }

## License

GPLv3

## Author Information

This role was created in 2016 by [Florian Schwanz](https://interoberlin.de/).
