# cluster-control-panel

This procket is the source repo for the cluster control web application and service control scripts. 

the repo is split into two branches, frontend and worker. 

frontend contains configuration and install scripts for an API service endpoint to queue recordings to be processed by the worker nodes. This includes a FLASK server for accepting requests, and a RabbitMQ client for generating the work messsages. 



Worker is designed to be dropped on any ubuntu based machine with GPUs to add it to the ztelco compute cluster network. it will pull the nessacary repos and install compute drivers. This includes a web frontend for starting/stopping services, the control scripts to be run by the web frontend, database configuration information for tracking process states. 