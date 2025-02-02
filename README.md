# Simple HA setup

This is an ansible playbook that sets up a simple Home Assistant server.

This contains the following items:
- Basic server settings
    - Changing default SSH port
    - Use NTP for time
    - Turning on auto-updates
- Installing docker
- Setting up Home Assistant in docker
- Putting nginx as a reverse-proxy in front of it
- Setting up SimpleNotifier for Discord notifications
- Setting up Wireguard to access it from the outside
- Doing regular backups to a S3 storage

To generate the client config, be sure to have your `inventory.yaml` file correctly setup and run the `gen_wg_clients.py` file. They will be available in `./00_WIREGUARD_CLIENTS/{ansible_group}/{hostname}.conf`.

Note that this is a bare-bone Home Assistant designed for ease of use. There is no MQTT / NodeRED / Zigbee2MQTT yet.