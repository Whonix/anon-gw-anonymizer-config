# Tor Configuration and Tweaks for Anonymity Distributions #

Tor config file with distribution defaults (for stream isolation, etc.),
example user configurations and other tweaks required. The Tor binary
itself does not get modified.

Deactivates IPv4 forwarding using /etc/sysctl.d/
IPv4 forwarding is not required for a Tor based Anonymity Distribution
Gateways. Deactivating it as defense in depth to prevent leaks.

Deactivates IPv6 using /etc/sysctl.d/
There are no IPv6 Anonymity Distribution Gateways featuring an IPv6 firewall
yet. Therefore deactivating it to prevent leaks.

This package is produced independently of, and carries no guarantee from,
The Tor Project.
## How to install `anon-gw-anonymizer-config` using apt-get ##

1\. Download Whonix's Signing Key.

```
wget https://www.whonix.org/patrick.asc
```

Users can [check Whonix Signing Key](https://www.whonix.org/wiki/Whonix_Signing_Key) for better security.

2\. Add Whonix's signing key.

```
sudo cp ~/derivative.asc /usr/share/keyrings/derivative.asc
```

3\. Add Whonix's APT repository.

```
echo "deb [signed-by=/usr/share/keyrings/derivative.asc] https://deb.whonix.org bullseye main contrib non-free" | sudo tee /etc/apt/sources.list.d/derivative.list
```

4\. Update your package lists.

```
sudo apt-get update
```

5\. Install `anon-gw-anonymizer-config`.

```
sudo apt-get install anon-gw-anonymizer-config
```

## How to Build deb Package from Source Code ##

Can be build using standard Debian package build tools such as:

```
dpkg-buildpackage -b
```

See instructions. (Replace `generic-package` with the actual name of this package `anon-gw-anonymizer-config`.)

* **A)** [easy](https://www.whonix.org/wiki/Dev/Build_Documentation/generic-package/easy), _OR_
* **B)** [including verifying software signatures](https://www.whonix.org/wiki/Dev/Build_Documentation/generic-package)

## Contact ##

* [Free Forum Support](https://forums.whonix.org)
* [Professional Support](https://www.whonix.org/wiki/Professional_Support)

## Donate ##

`anon-gw-anonymizer-config` requires [donations](https://www.whonix.org/wiki/Donate) to stay alive!
