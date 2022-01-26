## Cloud Computing Fundamentals

Cloud Computing (5 Essential Characteristics)
* #1 - On-demand Self-Service
  * "...can provision capabilities as needed **_without requiring human interaction_**"
    * capabilities, in this context, means products or features (ie virtual machines, storage, databases, or networking)
    * self-serivce: you don't need to liase with a support or provisioning team 
    * on-demand: you don't need to inform the vendor days, weeks, or months in advance; you can provision any resource you want, without involving humans & without delay
* #2 - Broad Network Access
  * "capabilities are available over the **_network_** and accessed through **_standard mechanisms_**"
    * you can accesss services in AWS, Google, and Azure over a standard network using standard means (ie HTTP, HTTPS, SSH, Remote Desktop or maybe even using a VPN)
    * it's probably not cloud if:
      * you need to visit a DC or a vendor's facility to interact with your data/systems
      * you need a private network link to access your environment
* #3 - Resource Pooling
  * "There is a sense of **_location independence_**...no **_control_** or **_knowledge_** over the exact **_location_** of the resources" (1st part)
  * "...Resources are **_pooled_** to serve multiple consumers using a **_multi-tenant model_**" (2nd part)
  * Resource Pooling is about abstraction (1st part) & economies of scale (2nd part) (revisit later)
    * with AWS, you instruct the provider to deploy a virtual machine in a certain region, where they're free to use whatever data center they want, & whatever hardware vendor they want
      * this means the risks of this process are with the vendor (a good thing that historically was the cause of initial resistance to using cloud computing)
        * (can revisit later)
      * we've moved away from thinking of hardware as value to thinking of applications, data, & services, as the actual things of value that a business offers
  * the 2nd part of resource pooling definition defines how cloud vendors pool the needs of their customers together
    * instead of businesses buying for their own needs (ie 10 servers for company X, 10 servers for company Y), the cloud vendor might procure 10,000 servers for use for part of their customer base (larger scale means larger economies of scale) 
      * (revisit later)
    * pooling allows for easier scaling whenever a customer needs it
  * when communicating or using a platform such as AWS, Google, or Azure, instead of seeing a mention of "your servers" or "your storage", you allocate it from a pool & return it to that pool when it's no longer required, while the vendor is managing that capacity behind the scenes
  * what cloud does, is it has isolation between customers (your data is only visible to you)
    * one of the benefits of pooling: even though the cloud vendor is using pooling, & even though you & another business are probably sharing hardware, you would never know each other existed
* #4 - Rapid Elasticity
  * "Capabilities can be elastically provisioned & released to scale rapidly outward & inward with demand" (in this context, capabilities are resources)
  * "To the consumer, the capabilities available for provisioning often appear to be unlimited"
    * with elasticity, a system can start off small & when system load increases, the system size increases & when system load decreases, the system can reduce in size
    * (revisit later)
* #5 - Measured Service
  * "Resource usage can be **_monitored_**, **_controlled_**, **_reported_**, & **_BILLED_**"
