





7.0.3.0.ifix01

**This article was originaly published in 2019.06.11**


What’s New in UrbanCode Deploy 7.0.3.0.ifix01
=============================================








### Distributed Front End (DFE)




---



UrbanCode Deploy 7.0.3.0 offers support for a distributed front-end server, that will allow customers to spread the HTTP traffic across numerous front-end servers. This adds additional resiliency to your UrbanCode Deploy environment, while allowing for a better user experience and easier troubleshooting (and less impact) to potential UI issues. For more information, please see our blog post on [Distributed Front End.](https://developer.ibm.com/urbancode/2019/05/23/distributed-front-end-server/)

 
### Maintenance Mode




---



UrbanCode Deploy 7.0.3.0 now supports maintenance mode, which will assist in upgrades, patches, and general maintenance of your server. This mode allows the completion of existing deployments while preventing new ones from running. It also tracks any planned deployments during an outage and will notify users that their deployment did not take place due to server maintenance. For more information, please see our blog post on [Maintenance Mode.](https://developer.ibm.com/urbancode/2019/06/07/deploy-703-maintenance-mode/)

 
### Agent Logs Available in the UI




---



Users who are taking advantage of the new WebSocket server/agent communication will be able to now access agent logs from within the UrbanCode Deploy UI. For more information, please see our blog post on [Agent Logs](https://developer.ibm.com/urbancode/2019/05/15/urbancode-deploy-7-0-3-agent-logs-available/)

 
### “Not” Environment Gates




---



Users can now explicitly define that component versions with certain statuses should NOT be allowed into an environment. This makes it easy to mark a particular version as defective and ensure that it doesn’t accidentally get deployed to an environment it should not. For more information, please see our blog post on [Not Gates.](https://developer.ibm.com/urbancode/2019/05/30/introducing-deploy-not-environment-gates/)

 
### Agent Pool Algorithm




---



The agent pool algorithm has been updated to take into consideration the workload of a particular agent before assigning work. For more information, please see our blog post on [Agent Pools.](https://developer.ibm.com/urbancode/2019/05/08/blog-series-introducing-urbancode-deploy-7-0-3-agent-pools/)

 
### Generic Processes Enhancements




---



Starting in UrbanCode Deploy 7.0.3.0, users can now run Generic Processes through our REST API. Generic Processes can now also be ran against multiple resources at a time.

 
### Component Template Enhancement




---



Component Templates now contain an "Import Versions Automatically" option.



 














