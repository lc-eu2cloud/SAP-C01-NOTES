# Course Scenario #

## Animals4Life ORG ##

### Animal Rescue & Awareness Organization ###
* Overview
  * region-dependent animal rescue, medical care, habitat preservation for wild animals, and providing new homes for domestic animals
  * Monitoring (habitats, animal migration)
  * Technologies (IoT, Big Data)
  * Global company (HQ:Brisbane, Australia)
    * Other locations: London, New York, Seattle
    * Staff: ~100 remote field workers (animal care, vets, research scientists) located in regional Australia and other in-need locations; political lobbying staff (government policy)
    * Departments: call center, general admin, IT, legal, marketing, and accounts
  * Infrastructure
    * small on-prem DC in Brisbane; number of colos with 5 rented racks of space; old vendor-managed DC & vendor encouraging customers move out ASAP
    * AWS pilot in Sydney region lacking resiliency & scalability business needed
    * Azure/GCP isolated pilots lacking resilience & scalability business needed
    * All global offices and remote field workers consume resources from Brisbane office
  * cost-conscious but willing to try new things/adopt new technologies (business benefit required)

 * Current Problems
  * legacy on-premises is failing (DC will be decommissioned in 18 months)
  * Cloud pilots have been suboptimal and not best practice (AWS/Azure/GCP)
  * performance issues for remote field workers outside Brisbane area experiencing high latency
  * lack of HA and scalability hinders opportunity to grow at scale and adequately non-Australian staff & locations
  * skills gap with existing staff: little automation/experience with cloud development
  
