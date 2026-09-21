### Architecture of Opensnitch

#### UI
The architecture of OpenSnitch is quite simple, so this part of the documentation is intended mostly for new contributors looking for a way to start familiarizing with this project.

OpenSnitch seperates itself into a **Python + Qt** UI and a **Go / C** backend (for the actual firewall nodes).
The main UI initialization is done by `service.py` under `/ui/opensnitch` which uses `nodes.py` to manage the firewall backend nodes *(get / send notifications, read configuration, manage network rules)*

The UI of OpenSnitch also manages an SQLite database which is used to record events as seen by the UI, outside of what the backend logs by itself, which is what allows the GUI to display connections and events (etc).