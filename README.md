# Course Scenario #
## Animals4Life - Animal Rescue & Awareness Organization ##
* Overview
  * region-dependent animal rescue, medical care, wild animal habitat preservation, & providing new homes for domestic animals
  * Monitoring (habitat devastation worldwide, animal migration)
  * Technologies (IoT, Big Data)
  * Global company (HQ:Brisbane, Australia)
    * Other locations: London, New York, Seattle
    * Staff: ~100 remote field workers (animal care, vets, research scientists) located in Australian region & other in-need locations; political lobbying staff (government policy)
    * Departments: call center, general admin, IT, legal, marketing, & accounts
  * Infrastructure
    * small on-prem DC in Brisbane; colos with 5 rented racks of space; old vendor-managed DC & vendor encouraging customers move out ASAP
    * AWS pilot in Sydney region lacking resiliency & scalability business needed
    * Azure/GCP isolated pilots lacking resilience & scalability business needed
    * All global offices & remote field workers consume resources from Brisbane office
  * cost-conscious but willing to try new things/adopt new technologies (business benefit required)

 * Current Problems
   * legacy on-premises is failing (DC will be decommissioned in 18 months)
   * Cloud pilots have been suboptimal & not best practice (AWS/Azure/GCP)
   * performance issues for remote field workers outside Brisbane area experiencing high latency
   * lack of HA & scalability hinders opportunity to grow at scale & adequately support non-Australian staff & locations
   * skills gap with existing staff: little automation/experience with cloud development
   * Global expansion concerns - costs for new infrastructure (purchasing & deploying international infrastructure - very expensive)
 
 * Ideal Outcomes
   * fast performance for all field workers (not limited by systems business uses)
   * when required, deploying necessary operations into new regions quickly (provisioned/de-provisioned based on business needs;automation & usage-based billing)
   * low base infrastructure cost (allocate most of limited funds towards animal care) whilst able to scale & rapidly grow when required
   * Utilizing agility to leverage real-world events such as social media campaigns at short notice to draw attention to disasters or other issues worldwide (rapid provisioning)
   * creating solution architectures that support emerging technologies (IoT, Big Data, Machine Learning, analytics, etc.)
   * using automation to allow business to focus on core staff that deliver on the organization's mission; minimized costs for IT, legal, finance, & minimized need for additional IT staff 
  
