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



1. **<span style="text-decoration:underline;">Bronze Tier</span>**: SPs should report approximate location, water usage, and energy consumption data to the [Filecoin Green Reporting Portal](#bookmark=id.a3kb9cl12p8l) for auditing, calculate their emissions profile according to the market-based attributional carbon accounting approach, and should ethier: \

    1. match their energy consumption profile to Energy Attribution Credits (EACs) **<span style="text-decoration:underline;">on a annual basis</span>**, or \

    2. Provide evidence of green electricity products from their energy supplier (e.g. Green Tariffs) \

2. **<span style="text-decoration:underline;">Silver Tier:</span>** SPs should report approximate location, water usage, granular energy consumption data, hardware set-up to the [Filecoin Green Reporting Portal](#bookmark=id.a3kb9cl12p8l) for auditing, calculate their emissions profile according to the market-based attributional carbon accounting approach, and should match their energy consumption profile to EACs or GCs **<span style="text-decoration:underline;">on a quarterly basis</span>**. \

    3. <span style="text-decoration:underline;">Embodied Emissions</span>: Match hardware embodied emissions to high-quality carbon credits (removals or offsets).
3. **<span style="text-decoration:underline;">Gold Tier:</span>** SPs should report approximate location, water usage, granular energy consumption data, hardware set-up to the [Filecoin Green Reporting Portal](#bookmark=id.a3kb9cl12p8l) for auditing, calculate their emissions profile according to the consequential carbon accounting approach, and every unit of electricity used (MWh) must be accounted for by one of the following: \

    4. Onsite renewable energy generation, in which meter data is provided showing that consumption is matched by onsite generation on a 1-to-1 basis. \

    5. For consumption not matched by renewable onsite generation, emissions due to grid draw must be matched to avoided emissions accounted for by GCs, with a temporal resolution of one hour, obtained either through:
        1. Power Purchase Agreements (PPAs) for new generation
        2. GCs sold on the open market \

    1. <span style="text-decoration:underline;">Embodied Emissions</span>: Match hardware embodied emissions to high-quality carbon credits (removals or offsets).

Additional details on these three Tiers are provided in [Annex 2: Details on Storage Provider’s Tiered Sustainability Claims](#bookmark=id.j4nowpnymgs7). The information that follows is meant to inform Filecoin Storage Providers how to account for and report GHG emissions and electricity consumption, and how to make decisions about the procurement of renewable energy.

