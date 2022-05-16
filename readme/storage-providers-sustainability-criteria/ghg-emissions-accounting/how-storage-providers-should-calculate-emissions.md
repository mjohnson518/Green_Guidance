# How Storage Providers should Calculate Emissions

Below is guidance on the four necessary steps that Storage Providers should perform for conducting a comprehensive carbon accounting exercise:

* **Determine the ‘operational boundaries’ for reporting**: Storage Providers should set operational boundaries according to the _Control Approach_ for all facilities of which they have _financial and/or operational control_.\

  * For corporate emissions reporting, two approaches can be used to consolidate GHG emissions: the Equity Share and the Control approaches.
  * Storage Providers who own their entire operation should use the Control approach, because under this approach, a company accounts for 100 percent of the GHG emissions from operations over which it has control. It does not account for GHG emissions from operations in which it owns an interest but has no control.
  * Storage Providers who run operations in Colocation Data Centers should usually use the Equity approach, and calculate emissions based on the percent utilization of data center capacity.
  * When using the Control approach, Storage Providers should choose between either the _financial and/or operational control_ criteria.
  * Determining these boundaries is necessary because once energy is generated, it follows two possible paths: it is either consumed on-site, or distributed to another entity by direct line transfer or through the electricity grid. These pathways determine how the emissions from energy generation are accounted for and reported by different entities in scope 1 and 2. Therefore, it is necessary that Storage Providers use a consistent approach & criteria to defining this operational boundary over time across all operations.
  * Refer to [Chapter 3 of the GHG Protocol Corporate Standard](https://ghgprotocol.org/sites/default/files/standards/ghg-protocol-revised.pdf) and [Chapter 5 of the GHG Protocol Scope Guidance 2](https://ghgprotocol.org/sites/default/files/standards/ghg-protocol-revised.pdf) for more information on the three consolidation approaches for defining organizational boundaries.&#x20;
  * The following flowchart is intended to guide SPs through the Operational Boundary decision-making process:

![(source)](https://lh4.googleusercontent.com/TVq11SE52M\_-opEhs7Aq\_UXmX4YT3WADupWao0aBj6FtDVz-MP91mbjKUTmr6uA6RrQ9xdNKOOxw4YqqvqkI80slypy8hUkHXnNt\_81hlxGUknyVtZ29CTXWvi9TX4kKwQzzeuTTR4Jo6znnPQ)

*   **Obtain activity data (i.e., electricity consumption) for the reporting period**: After operational boundaries are defined, the next step is obtaining activity data, i.e. the details of all electricity acquired and consumed.&#x20;



    * The best source of activity data is metered electricity consumption, electricity utility bills, and reports that document electricity consumption in megawatt-hours (MWh) or kilowatt-hours (kWh).
    * The activity data and information that SPs can submit may include, but is not limited to:\

      * Relevant minerIDs (to estimate bounds on power use)
      * Geolocation - approximate location via zip or postal code
      * Monthly electricity bills
      * Granular electricity use measurements, if available
      * Electricity meter ID, if applicable
      * Documentation of equipment purchases (to substantiate efficiency claims)
      * Photo or video of setup, or video tour with auditor
      * Documentation of renewable energy purchases
      * An agreement that output data can be made public, or note opting out of some datasets\

    * Submitted information will be used for verifying SPs' energy use and hardware performance. If activity data is not available, SPs' should use the best possible estimation and, ideally, should publish their estimation methodology (e.g., include transparent documentation of the assumptions and rationale behind any estimations).
    * The Filecoin Green team has already developed a robust **** [**methodology**](https://filecoin.energy/methodology) and [**Dashboard**](https://filecoin.energy/) **** for estimating power use of the entire network and individual Storage Providers, and can assist SPs' in determining appropriate estimates if they do not have them. \

* **Determine electricity grid emissions factors**: The next step is obtaining the electricity grid emissions intensity figure (i.e., emissions factor) to use with the reported activity data.\

  * Storage Providers should choose emission factors according to the following hierarchy and should seek to use the highest-ranked option possible under each of the three approaches:
    * First Option: **Consequential Approach** - uses Marginal Emissions Factors to understand how overall system emissions change through your actions.
    * Second Option: **Market-based Attributional Approach** - takes into account green energy purchases, such as renewable PPA’s, or EAC’s/REC’s.
    * Third Option: **Location-based Attributional Approach** - uses average emissions factors based on the generation mix of the local grid.\

  * At this point it's worth noting that SPs' should use lower-ranked options only if higher ones are unavailable, and that the most holistic emissions calculation can be achieved by combining the first and second options (Consequential and Market-based).\

  * ****[**Annex 1: Carbon Accounting Methodologies Hierarchy**](../../annex-1-carbon-accounting-methodologies-hierarchy.md) provides an overview of the necessary substeps for determining electricity grid emissions factors based on the three ranked methods.\

* **Match emissions factors and electricity consumption:** The fourth step in accounting for emissions from SPs' operations is matching the emissions factors to each unit of electricity consumed. This is a straight-forward process, but differs slightly depending on the accounting approach employed.\

  * For the **Consequential Approach**, SPs should match each unit of electricity to the appropriate emission factor based on both their physical location and duration of time for each reporting period. If marginal emissions factors are not available for specific locations, SPs should use the default grid emissions factors for their specific country, region, or jurisdiction.
  * For the **Market-based Attributional Approach**, SPs should choose a specific information source, with its corresponding emission factor, for each unit of electricity. For example, if a SP has purchased enough RECs to cover one third of their electricity use, they will need to use other instruments or information on the emission factor hierarchy to calculate the emissions for the remaining two thirds.
  * For the **Location-based Attributional Approach**, SPs should match units of electricity consumption to the appropriate emission factors based on the location(s) in which they are consumed. While difficult in many jurisdictions, SPs should also seek to map data to emission factors based on the specific duration of time for their reporting period, especially if using real-time emission factors and real-time electricity data.

Once these four steps have been conducted, the final step is to calculate total emissions by multiplying each section of activity data by the appropriate emission factor, for each applicable GHG. Electricity emission factor sets generally include factors for carbon dioxide (CO2), methane (CH4), and nitrous oxide (N2O).

Once activity data is multiplied by the appropriate emissions factors for specific GHGs, then multiply these GHG emission totals by the appropriate global warming potential (GWP) values to get total emission in metric tons CO2 equivalent (CO2 e). GWPs are multipliers applied to greenhouse gasses such as methane (CH4) and Nitrous Oxide (N2O) to equate the impact they have on the Earth’s temperature with that of Carbon Dioxide (CO2). The IPCC updates GWP values during the development of each Assessment Report. The table below lists the most current GWP’s:

![(source)](https://lh4.googleusercontent.com/DeHHPDvtRvtx\_NTGSXBLOsO146jSbO9pEphPA4GctPnNN-S6lFmC1PuG0f9JAC2nGzxWVkiZGgPPngX1TJcVEaNHab-0pCa0KwRHLsZdCqV2WNJz3whyl53IV5siNhWUHRN7gRqo9Wz0wt008Q)
