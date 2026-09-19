### Architecture of Opensnitch
Opensnitch seperates itself into a **Python + Qt** UI and a **Go / C** backend for the actual firewall nodes.
The main UI initialization is done by `service.py` under `/ui/opensnitch` which uses `nodes.py` to manage the firewall backend nodes *(get / send notifications, read configuration, manage network rules)*