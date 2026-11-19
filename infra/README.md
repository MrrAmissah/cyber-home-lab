# Lab infrastructure

Definitions for bringing the lab up reproducibly. Planned layout is in `docs/network-diagram.md`.

- `vagrant/` or `compose/` — VM and container definitions (to come)
- `firewall/` — pfSense rule export, with a table of every permitted flow and its reason
- `baselines/` — hardening baselines applied to lab hosts

Images, ISOs and VM disks are never committed (see `.gitignore`); this folder holds only text definitions.
