# Course Scenario #
## Animals4Life - Animal Rescue & Awareness Organization ##
* Overview
  * region-dependent animal rescue, medical care, wild animal habitat preservation, & providing new homes for domestic animals
  * Monitoring (animal migration, habitat devastation worldwide)
  * Technologies (Big Data, IoT)
  * Global organization (HQ:Brisbane, Australia)
    * Other locations: London, New York, Seattle
    * Staff: ~100 remote field workers (animal care, vets, research scientists) located in Australian region, other in-need locations & political lobbying staff (government policy)
    * Departments: call center, general admin, IT, legal, marketing, & accounts
  * Infrastructure
    * Brisbane: small on-prem DC (5 rented racks of space in colos), DC: old, vendor-managed & customers encouraged to move out ASAP
    * AWS pilot in Sydney region, isolated Azure/GCP pilots, all failed to meet scalability & resiliency organization needed
    * Brisbane office: source of all resource consumption for global offices & remote field workers
  * cost-conscious & willing to try new things/adopt new technologies => business benefit

 * Current Problems
   * legacy on-premises is failing & DC will be decommissioned in 18 months 
   * Cloud pilots: suboptimal & not best practice (AWS/Azure/GCP)
   * performance issues for remote field workers outside Brisbane area experiencing high latency
   * lack of HA & scalability hinders opportunity to grow at scale & adequately support non-Australian staff & locations
   * skills gap with existing staff: little automation/experience with cloud development
   * Global expansion concerns - costs for new infrastructure very expensive (purchasing & deploying international infrastructure)
 
 * Ideal Outcomes
   * fast performance for all field workers (not limited by systems organization uses)
   * deploying necessary operations into new regions quickly whem required (provisioned/de-provisioned based on business needs;automation & usage-based billing)
   * low base infrastructure cost (allocate most of limited funds towards animal care) whilst able to scale & rapidly grow when required
   * Utilizing agility to leverage real-world events such as social media campaigns at short notice to draw attention to disasters or other issues worldwide (rapid provisioning)
   * creating solution architectures that support emerging technologies (IoT, Big Data, Machine Learning, analytics, etc.)
   * using automation to allow business to focus on core staff that deliver on the organization's mission; minimized costs for IT, legal, finance, & minimized need for additional IT staff 
  
