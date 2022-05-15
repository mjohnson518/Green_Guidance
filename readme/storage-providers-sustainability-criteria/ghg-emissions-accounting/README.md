# GHG Emissions Accounting

To achieve any credible decarbonization goals, actors must start with a comprehensive carbon accounting exercise, and in order to do so they must have a robust way to measure, track, and report their electricity use and the associated GHG Emissions.

[Carbon accounting](https://en.wikipedia.org/wiki/Carbon\_accounting) is the process by which organizations inventory and audit the greenhouse gasses (GHGs) they generate, including those the organization is directly and indirectly responsible for emitting. This process allows organizations to better understand and manage the climate impacts of their operations, and may be used to inform business strategy and decision-making.

The most widely used approach for carbon accounting is the [Greenhouse Gas Protocol](https://ghgprotocol.org/), a joint initiative by the nonprofits [WRI (World Resources Institute)](https://www.wri.org/) and [WBCSD (World Business Council for Sustainable Development)](https://www.wbcsd.org/). The GHG Protocol defines three “Scopes” of emissions for GHG accounting and reporting purposes:

* **Scope 1**: Direct emissions that result from an organization’s activities, such as fuel combustion from facilities.
* **Scope 2**: Indirect emissions associated with an organization’s activities, often from the generation of purchased electricity consumed by your company.
* **Scope 3**: Indirect emissions from an organization’s supply chain (rather that its primary operations), such as embodied emissions in purchased raw materials.

In the context of Filecoin, Storage Providers are responsible for the emissions that result from the direct activities of their company (Scope 1), those which result from the generation of purchased electricity consumed by their organization (Scope 2), as well as a portion of the emissions from all other indirect sources of emissions from an organization’s supply chain (Scope 3).

A major component of these emissions results from the electricity which SPs use to store data and prove that it is stored over time. These emissions are generated from the electricity consumption of their hard disk drives (HDDs) for [Sealing](https://spec.filecoin.io/#section-glossary.seal) data and solid-state drives (SSDs) for [Storing](https://spec.filecoin.io/#section-glossary.storage-miner-actor) data.
