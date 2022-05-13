# Green\_Guidance

Filecoin Storage Providers (SPs) would benefit from guidance around how to approach sustainable operations. A guidance document should lay out best practices from carbon accounting, renewable energy procurement, and related industries in order to suggest how to approach sustainable operations. This content is based on the [Filecoin Green Tools Issue #5](https://github.com/protocol/FilecoinGreen-tools/blob/main/0005-FGTP-Green-SP-Guidance.md)


# Filecoin Green Storage Providers Guidance Documentation

**March, 2022**

## Introduction

The [United Nations Environmental Programme's 2021 Emissions Gap Report](https://www.unep.org/resources/emissions-gap-report-2021) highlights that climate change is no longer a future problem. It is a '_now_' problem. The [Intergovernmental Panel on Climate Change (IPCC) Sixth Assessment Report (AR6)](https://www.ipcc.ch/assessment-report/ar6/) further demonstrates that many of the extreme weather events experienced around the world today can be attributed to the build-up of anthropogenic greenhouse gas (GHG) emissions in the atmosphere.

Considered a “code red for humanity” by the United Nations Secretary-General, the IPCC AR6 report documents that unless there are immediate, rapid and large-scale reductions in global GHG emissions, limiting warming to 1.5°C or even 2°C by the end of the century will be beyond reach. 

The message is clear: to ensure we maintain a livable climate, society must radically & rapidly decarbonize the global economy. This imperative necessitates the collective efforts of countries, corporations, and consumers to realign incentives and drive decarbonization efforts at a scale and speed never before achieved.

Luckily, there are signs of hope. Research by the [Climate Intelligence Team at RMI](https://rmi.org/our-work/climate-intelligence/) shows that Governments - local, regional, and national - are drafting rules to [mandate climate risk disclosures](https://www.sec.gov/news/press-release/2022-46), and policymakers have [begun implementing](https://ec.europa.eu/taxation_customs/green-taxation-0/carbon-border-adjustment-mechanism_enle-business/britains-former-trade-secretary-calls-carbon-border-tax-2021-05-26/) carbon adjustments at National borders. More than half of S&P 500 companies have sustainability goals, including [science-based targets](https://sciencebasedtargets.org/sbti-progress-report-2020) for GHG emissions reduction. Financial institutions and their regulators are beginning to explicitly [incorporate ](https://www.reuters.com/business/sustainable-business/global-regulators-refine-climate-fallout-banks-2021-04-14/)climate risks into decision-making frameworks, and there are now over 2,600 signatories to the [Task Force on Climate-Related Financial Disclosures](https://www.fsb.org/wp-content/uploads/P141021-1.pdf). Yet, underlying all of these actions are two simple questions: will this be enough, and how can we track real progress?

The answers to those questions may come from the nascent Web3 Industry. Blockchain networks and crypto-primitives have a unique opportunity to drive collective action toward reducing emissions, showcasing industry-wide decarbonization, and creating new demand for clean technologies. In doing so, the industry can become an important player in the renewable energy space, and can help drive objective, actionable change towards environmental sustainability.

## Filecoin Green

In recognition of this decarbonization imperative, Protocol Labs launched [Filecoin Green](https://green.filecoin.io), an initiative focused on building web3-native monitoring and reporting tools for publicly verifiable environmental claims. 

Our plan is simple: we are building the tools to measure the environmental impacts of Filecoin and verifiably drive them below zero, building infrastructure along the way that can be leveraged by anyone to make transparent and substantive environmental claims for their own operations. 

We’re doing this by connecting the entire network to renewable energy, allowing each individual Filecoin Storage Provider to publicly prove their source of electricity. We made Filecoin the world’s most transparent blockchain when it comes to electricity consumption, and built the [filecoin.energy](https://filecoin.energy/) dashboard to raise the bar for energy transparency, allowing anyone to estimate the energy use of any node in the network. 

We leverage energy attribute certificates (EACs) to publicly prove that individual Filecoin nodes are buying renewable energy from generators in their region, recording these purchases in [Filrep](https://filrep.io/?columns=energy&order=desc&sortBy=energy), a reputation system that stores data on the Filecoin network, and in the [filecoin.energy](https://filecoin.energy/) dashboard. Each record keeps track of where the energy was produced and proves the ownership of the corresponding EACs. Right now, the Filecoin Green team has procured EACs for just over [~2%](https://filecoin.energy/?charts=3-day_4-day&end=2022-03-27&start=2020-07-01) of the network's electricity consumption needs, and we’re aiming to match the entire network’s energy use with renewables by the end of Q2 2022.

In addition to buying renewable energy from existing projects, in 2021 we [mobilized $38M of capital to build new solar generation in the US](https://www.prnewswire.com/news-releases/protocol-labs-and-nelnet-announce-38-million-renewable-energy-fund-focused-on-investments-in-solar-energy-301485254.html). This will generate more renewable electricity on a yearly basis than the Filecoin network uses in the US, helping to decarbonize the power grid. 

Lastly, we’re building a substantial grants pipeline to catalyze the development of projects seeking to prove environmental claims in the Web3 industry. And yet, the most exciting thing about all of this is that we’re just getting started. In the calendar year 2022, we have ambitious plans to match storage providers with renewables every hour, allow developers storing data on Filecoin to prove their carbon footprint, and to drive the total emissions of the network below zero. 

Our goal is to make it as simple as possible for every Filecoin Storage Provider to provably showcase how they are accounting for and reducing the environmental impacts of their operations, laying out a pathway to sustainability for the network.


## Filecoin Green Pledge 

Moving forward past 2022, to encourage collective decarbonization efforts across the Filecoin network, the Filecoin Green Team has created the Filecoin Green Pledge (FGP), a first of its kind pledge that Filecoin Storage Providers may make to showcase their commitment to sustainability across their global operations. Adhering to the FGP means that Storage Providers are committed to: \




* 80% renewable electricity procurement by EOFY[^1] 2023


* 100% renewable electricity procurement by EOFY 2025 
* Maintaining 100% renewable electricity procurement on a continuous basis from thereon

These percentage thresholds, defined as the portion of renewable electricity over total electricity use, must be _<span style="text-decoration:underline;">publicly verifiable</span>_, meaning that they must be able to _<span style="text-decoration:underline;">demonstrate a cryptographic proof of an exclusive claim to use of unique renewable electricity generation</span>_ to meet the threshold percentages of their reported electricity usage, and must apply across all their global operations. 

We have set these stringent thresholds because, due to the evolving regulatory landscape, we are confident that recording and reporting on the proportion of renewable energy used against the overall energy consumption will become a mandatory monitoring and reporting requirement for many jurisdictions in the near future. If all Storage Providers adhere to the FGP, the Filecoin Green team is confident that the entire Filecoin network will be **<span style="text-decoration:underline;">100% carbon neutral by EOFY 2025.</span>** 

This timeline is in-line with many legacy industry actors, such as Microsoft[^2] and Amazon Web Services[^3], and quicker than other web3 initiatives, such as the Crypto Climate Accord[^4].

To incentivize Storage Providers to meet these threshold requirements, the Filecoin Green team has determined tiers of compliance, which, if met, may qualify SPs in the future to receive incentives such as Filecoin Plus datacap allocations, Reputation Score boosts, or loans. Details of these incentives will be determined in the future.

The Filecoin Reputation Score is meant to quantify, through a single number, the reliability of a Storage Provider for storage and retrieval deals so that clients can make informed decisions when selecting a miner. If sustainability criteria are added to the Reputation Score matrix, Filecoin Green will incentivize Storage Providers to decarbonize their operations by procuring more renewable energy. The information below explains the procedures and criteria we’ve set for SPs to showcase adherence to, and compliance for, the FGP and publicly verifiable sustainability claims.


## Storage Provider’s Tiered Sustainability Claims

In order to comply with the FGP, Storage Providers can make Sustainability claims in three (3) ways, each of which requires SPs to report audited approximate location, energy consumption, and renewable production data on a regular basis. The three types of Sustainability Claims follow a tiered hierarchy according to how granular the information is. The more rigorous the reporting and auditing procedures, the greater the Filecoin Plus datacap allocations and Reputation Score boosts the Storage Provider stands to receive. It is worth noting that these requirements are subject to change, and increase over time. The three tiers of Sustainability Claims follow the hierarchy listed below:



1. **<span style="text-decoration:underline;">Bronze Tier</span>**: SPs should report approximate location, water usage, and energy consumption data to the [Filecoin Green Reporting Portal](#bookmark=id.a3kb9cl12p8l) for auditing, calculate their emissions profile according to the market-based attributional carbon accounting approach, and should ethier: 

    1. match their energy consumption profile to Energy Attribution Credits (EACs) **<span style="text-decoration:underline;">on a annual basis</span>**, or \

    2. Provide evidence of green electricity products from their energy supplier (e.g. Green Tariffs) \

2. **<span style="text-decoration:underline;">Silver Tier:</span>** SPs should report approximate location, water usage, granular energy consumption data, hardware set-up to the [Filecoin Green Reporting Portal](#bookmark=id.a3kb9cl12p8l) for auditing, calculate their emissions profile according to the market-based attributional carbon accounting approach, and should match their energy consumption profile to EACs or GCs **<span style="text-decoration:underline;">on a quarterly basis</span>**. 

    3. <span style="text-decoration:underline;">Embodied Emissions</span>: Match hardware embodied emissions to high-quality carbon credits (removals or offsets).
3. **<span style="text-decoration:underline;">Gold Tier:</span>** SPs should report approximate location, water usage, granular energy consumption data, hardware set-up to the [Filecoin Green Reporting Portal](#bookmark=id.a3kb9cl12p8l) for auditing, calculate their emissions profile according to the consequential carbon accounting approach, and every unit of electricity used (MWh) must be accounted for by one of the following: 

    4. Onsite renewable energy generation, in which meter data is provided showing that consumption is matched by onsite generation on a 1-to-1 basis. 

    5. For consumption not matched by renewable onsite generation, emissions due to grid draw must be matched to avoided emissions accounted for by GCs, with a temporal resolution of one hour, obtained either through:
        1. Power Purchase Agreements (PPAs) for new generation
        2. GCs sold on the open market 

    1. <span style="text-decoration:underline;">Embodied Emissions</span>: Match hardware embodied emissions to high-quality carbon credits (removals or offsets).

Additional details on these three Tiers are provided in [Annex 2: Details on Storage Provider’s Tiered Sustainability Claims](#bookmark=id.j4nowpnymgs7). The information that follows is meant to inform Filecoin Storage Providers how to account for and report GHG emissions and electricity consumption, and how to make decisions about the procurement of renewable energy.

## Storage Providers Sustainability Criteria

The criteria and procedures specified here are intended to define (1) what constitutes a comprehensive carbon accounting exercise (covering Scopes 1, 2, & 3), and (2) how to source renewable electricity for the purposes of environmental disclosures or ESG reporting mechanisms. 

The contents herein draw inspiration from the [Crypto Climate Accord’s Carbon Accounting Guidance Documentation](https://cryptoclimate.org/wp-content/uploads/2021/12/RMI-CIP-CCA-Guidance-Documentation-Dec15.pdf), the [GHG Protocol Corporate Standards, Mitigation Goal Standard, Corporate Value Chain (Scope 3) Standard](https://ghgprotocol.org/standards), [GHG Protocol: Guidelines for Quantifying GHG Reductions from Grid-connected Projects](https://wriorg.s3.amazonaws.com/s3fs-public/pdf/ghgprotocol-electricity.pdf), [WattTime Emissionality paper](https://energyathaas.files.wordpress.com/2019/04/acdb3-00main.pdf), [SBTi’s Criteria and Recommendations](https://sciencebasedtargets.org/resources/files/SBTi-criteria.pdf), [CDP’s RE100 Documentation on Making Credible Renewable Electricity Usage Claims](https://www.there100.org/sites/re100/files/2020-09/RE100%20Making%20Credible%20Claims.pdf) and [accompanying Technical Criteria](https://www.there100.org/sites/re100/files/2021-03/RE100%20Technical%20criteria%20_for%20website_final.pdf). 


### GHG Emissions Accounting

To achieve any credible decarbonization goals, actors must start with a comprehensive carbon accounting exercise, and in order to do so they must have a robust way to measure, track, and report their electricity use and the associated GHG Emissions. 

[Carbon accounting](https://en.wikipedia.org/wiki/Carbon_accounting) is the process by which organizations inventory and audit the greenhouse gasses (GHGs) they generate, including those the organization is directly and indirectly responsible for emitting. This process allows organizations to better understand and manage the climate impacts of their operations, and may be used to inform business strategy and decision-making.

The most widely used approach for carbon accounting is the [Greenhouse Gas Protocol](https://ghgprotocol.org/), a joint initiative by the nonprofits [WRI (World Resources Institute)](https://www.wri.org/) and [WBCSD (World Business Council for Sustainable Development)](https://www.wbcsd.org/). The GHG Protocol defines three “Scopes” of emissions for GHG accounting and reporting purposes: 



* <span style="text-decoration:underline;">Scope 1</span>:  Direct emissions that result from an organization’s activities, such as fuel combustion from facilities 

* <span style="text-decoration:underline;">Scope 2</span>: Indirect emissions associated with an organization’s activities, often from the generation of purchased electricity consumed by your company

* <span style="text-decoration:underline;">Scope 3</span>: Indirect emissions from an organization’s supply chain (rather that its primary operations), such as embodied emissions in purchased raw materials

In the context of Filecoin, Storage Providers are responsible for the emissions that result from the direct activities of their company (Scope 1), those which result from the generation of purchased electricity consumed by their organization (Scope 2), as well as a portion of the emissions from all other indirect sources of emissions from an organization’s supply chain (Scope 3). 

A major component of these emissions results from the electricity which SPs use to store data and prove that it is stored over time. These emissions are generated from the electricity consumption of their hard disk drives (HDDs) for [Sealing](https://spec.filecoin.io/#section-glossary.seal) data and solid-state drives (SSDs) for [Storing](https://spec.filecoin.io/#section-glossary.storage-miner-actor) data.

#### How Storage Providers should Calculate Emissions

Below is guidance on the four necessary steps that Storage Providers should perform for conducting a comprehensive carbon accounting exercise:



* **<span style="text-decoration:underline;">Determine the ‘operational boundaries’ for reporting</span>**: Storage Providers should set operational boundaries according to the _Control Approach_ for all facilities of which they have _financial and/or operational control_.  \

    * For corporate emissions reporting, two approaches can be used to consolidate GHG emissions: the Equity Share and the Control approaches. \

    * Storage Providers who own their entire operation should use the Control approach, because under this approach, a company accounts for 100 percent of the GHG emissions from operations over which it has control. It does not account for GHG emissions from operations in which it owns an interest but has no control. \

    * Storage Providers who run operations in Colocation Data Centers should usually use the Equity approach, and calculate emissions based on the percent utilization of data center capacity. \

    * When using the Control approach, Storage Providers should choose between either the _<span style="text-decoration:underline;">financial and/or operational control</span>_ criteria. \

    * Determining these boundaries is necessary because once energy is generated, it follows two possible paths: it is either consumed on-site, or distributed to another entity by direct line transfer or through the electricity grid. These pathways determine how the emissions from energy generation are accounted for and reported by different entities in scope 1 and 2. Therefore, it is necessary that Storage Providers use a consistent approach & criteria to defining this operational boundary over time across all operations
    * Refer to [Chapter 3 of the GHG Protocol Corporate Standard](https://ghgprotocol.org/sites/default/files/standards/ghg-protocol-revised.pdf) and [Chapter 5 of the GHG Protocol Scope Guidance 2](https://ghgprotocol.org/sites/default/files/standards/ghg-protocol-revised.pdf) for more information on the three consolidation approaches for defining organizational boundaries. \

    * The following flowchart is intended to guide SPs through the Operational Boundary decision-making process:



<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image1.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image1.png "image_tooltip")


<p style="text-align: right">
<em>(<a href="https://www.hess.com/docs/default-source/sustainability/hess-corporation-greenhouse-gas-inventory-protocol.pdf?sfvrsn=ffe47f6b_8">source</a>)</em> \
</p>




* **<span style="text-decoration:underline;">Obtain activity data (i.e., electricity consumption) for the reporting period</span>**: After operational boundaries are defined, the next step is obtaining activity data, i.e. the details of all electricity acquired and consumed.  \

    * The best source of activity data is metered electricity consumption, electricity utility bills, and reports that document electricity consumption in megawatt-hours (MWh) or kilowatt-hours (kWh).  \

    * The activity data and information that SPs can submit may include, but is not limited to: \

            * Relevant minerIDs (to estimate bounds on power use)
            * Geolocation - approximate location via zip or postal code
            * Monthly electricity bills
            * Granular electricity use measurements, if available
            * Electricity meter ID, if applicable
            * Documentation of equipment purchases (to substantiate efficiency claims)
            * Photo or video of setup, or video tour with auditor
            * Documentation of renewable energy purchases
            * An agreement that output data can be made public, or note opting out of some datasets \

    * Submitted information will be used for verifying SPs' energy use and hardware performance. If activity data is not available, SPs' should use the best possible estimation and, ideally, should publish their estimation methodology (e.g., include transparent documentation of the assumptions and rationale behind any estimations). \
 
    * The Filecoin Green team has already developed a robust [methodology](https://filecoin.energy/methodology) and [Dashboard](https://filecoin.energy/) for estimating power use of the entire network and individual Storage Providers, and can assist SPs' in determining appropriate estimates if they do not have them. \

* **<span style="text-decoration:underline;">Determine electricity grid emissions factors</span>**: The next step is obtaining the electricity grid emissions intensity figure (i.e., emissions factor) to use with the reported activity data. 
    * Storage Providers should choose emission factors according to the following hierarchy and should seek to use the highest-ranked option possible under each of the three approaches: \
 
            * <span style="text-decoration:underline;">First Option</span>: Consequential Approach - uses Marginal Emissions Factors to understand how overall system emissions change through your actions. \

            * <span style="text-decoration:underline;">Second Option</span>: Market-based Attributional Approach - takes into account green energy purchases, such as renewable PPA’s, or EAC’s/REC’s. \

            * <span style="text-decoration:underline;">Third Option</span>: Location-based Attributional Approach - uses average emissions factors based on the generation mix of the local grid. \

    * At this point it's worth noting that SPs' should use lower-ranked options only if higher ones are unavailable, and that the most holistic emissions calculation can be achieved by combining the first and second options (Consequential and Market-based).  \

    * [Annex 1: Carbon Accounting Methodologies Hierarchy](#bookmark=id.fpgn9jkce160) provides an overview of the necessary substeps for determining electricity grid emissions factors based on the three ranked methods. \

* **<span style="text-decoration:underline;">Match emissions factors and electricity consumption:</span>** The fourth step in accounting for emissions from SPs' operations is matching the emissions factors to each unit of electricity consumed. This is a straight-forward process, but differs slightly depending on the accounting approach employed. \

    * For the **Consequential Approach**, SPs should match each unit of electricity to the appropriate emission factor based on both their physical location and duration of time for each reporting period. If marginal emissions factors are not available for specific locations, SPs should use the default grid emissions factors for their specific country, region, or jurisdiction. \

    * For the **Market-based Attributional Approach**, SPs should choose a specific information source, with its corresponding emission factor, for each unit of electricity. For example, if a SP has purchased enough RECs to cover one third of their electricity use, they will need to use other instruments or information on the emission factor hierarchy to calculate the emissions for the remaining two thirds. \

    * For the** Location-based Attributional Approach**, SPs should match units of electricity consumption to the appropriate emission factors based on the location(s) in which they are consumed. While difficult in many jurisdictions, SPs should also seek to map data to emission factors based on the specific duration of time for their reporting period, especially if using real-time emission factors and real-time electricity data.

Once these four steps have been conducted, the final step is to calculate total emissions by multiplying each section of activity data by the appropriate emission factor, for each applicable GHG. Electricity emission factor sets generally include factors for carbon dioxide (CO2), methane (CH4), and nitrous oxide (N2O). 

Once activity data is multiplied by the appropriate emissions factors for specific GHGs, then multiply these GHG emission totals by the appropriate global warming potential (GWP) values to get total emission in metric tons CO2 equivalent (CO2 e). GWPs are multipliers applied to greenhouse gasses such as methane (CH4) and Nitrous Oxide (N2O) to equate the impact they have on the Earth’s temperature with that of Carbon Dioxide (CO2). The IPCC updates GWP values during the development of each Assessment Report. The table below lists the most current GWP’s:



<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image2.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image2.png "image_tooltip")


<p style="text-align: right">
<em>(<a href="https://www.ercevolution.energy/ipcc-sixth-assessment-report/">source</a>)</em></p>

