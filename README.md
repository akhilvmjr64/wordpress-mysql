# Relases:
Version: `1.0.0`

# Usage:
One can directly use this helm package by downloading it and running the command `helm install <name-for-installation> <path-to-chart>` where `<name-for-installation>` is the name for the local installation, and `<path-to-chart>` directory where the chart is downloaded.

# Configurable Parameters:
- `wordpress`: For config related to wordpress webserver server
- `wordpress.dplyname`: Name for the webserver deployment
- `wordpress.replicas`: Number of webserver replicas
- `wordpress.lbname`: Name of loadbalancer for webserver i.e. service
- `wordpress.port`: Port number for the Node Port. Values must range in between 30000 and 32768
- `wordpress.pvc`: For config related to pvc of the webserver. This is done to share the server side sessions among the webservers.
- `wordpress.pvc.name`: Name for the webserver pvc.
- `wordpress.pvc.size`: Size of the webserver pvc

- `db`: For config related to mysql database server
- `db.dplyname`: Name for the database server deployment
- `db.replicas`: Number of database server replicas. Value accepted in version `1.0.0` is only 1.
- `db.lbname`: Name of loadbalancer for database server i.e. service
- `db.pvc`: For config related to pvc of the database server. This is done to make the data persistant.
- `db.pvc.name`: Name for the database server pvc.
- `db.pvc.size`: Size of the database server pvc.