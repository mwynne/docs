
## Goals

**Domain**
IT Automation

**Commands**
Example User Story:

_User:_
- "How many node resources do I have with at least 2GB of RAM and 2 CPUs?"
_Model Response:_
- "You have 5 nodes containing at least 2 GB of RAM and 2 CPUs:
	    1. Node identified by MAC 00:01:02:FF:FF:00 meets the criteria
	    2. Node identified by MAC 00:01:02:FF:FF:01 has 4 GB of RAM and 4 CPUs
	    3. Node identified by MAC 00:01:02:FF:FF:02 has 8 GB of RAM and 4 CPUs
	    4. Node identified by MAC 00:01:02:FF:FF:03 has 24 GB of RAM and 16 CPUs
	    5. Node identified by MAC 00:01:02:FF:FF:04 has 128 GB of RAM and 64 CPUs"
_User:_
- "Create an NGINX server on a node with resources that are nearest 2GB of RAM and 2 CPUs. Name it nginx001."
_Model Response:_
- "I have selected the node identified by MAC 00:01:02:FF:FF:00, which most closely matches the specified criteria. Since you have not provided any further details, I will deploy the default configuration for NGINX on the latest Ubuntu LTS distribution and set the host name of node 00:01:02:FF:FF:00 to nginx001. This task will be executed asynchronously and I will notify you when it is complete. Is this what you intended and do you wish to continue?"
_User:_
- "Yes"
_Model Response:_
- "Proceeding. You may inquire as to the status of this task at any time by simply asking me."
_..._ some time later _..._
_User:_
- "What is the status with the deployment of nginx001?"
_Model Response:_
- "Currently, the machine is being provisioned with fresh install of Ubuntu 22.04.03. I estimate the remaining time to complete this task is about 5 minutes."
_..._ some time later _..._
_Model Response:_
- "The deployment of NGNIX on nginx001 is now complete.
	- "FQDN: nginx001.iac-ng.net"
	- "IP: 10.10.0.20"
	- "Default NGNIX configuration is listening on port 80
	Do you wish for any additional information on this resource?"
_User:_
- "No"
_User:_
- "Please enable health and telemetry monitoring on nginx001. Send me a notification via email if the health status changes."
_Response:_
- "I would be happy to do so. How long do you want me to keep monitoring data before disposing of it?"
_User:_
- "30 days"
_Response:_
- "Very well. Monitoring is enabled and you will receive a notification if the health status changes."

**Success Criteria (PoC)**
- Correctly handle the user story above



- Distributed & Routed (like IP)
- Every node or resource knows about or can query other resources, either directly or indirectly
- Broadcast segments?
- Natural Language Generative AI model interface
- Suggest a sequence of tasks/commands/scripts be executed to achieve the desired outcome 
- Human to confirm
- Detailed system information gathering
- ZeroMQ-based? 
- System information is tracked in a natural language format
- The natural language documentation is the code