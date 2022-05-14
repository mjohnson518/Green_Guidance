# Annex 3: Filecoin Green Reporting Portal

As stated in the ‘_Obtain Activity Data_’ portion of [How Storage Providers should Calculate Emissions](https://docs.google.com/document/d/1neZhOecLC8\_03dnpY3yXwyhUihHx9PgONITH4sbeUo4/edit#bookmark=id.gth8sf352989) section, Filecoin Green is working on a comprehensive auditing process for all activity data, allowing SPs interested in making strong sustainability claims to publicly verify the associated data. We are building a Reporting Portal, which is an upload utility to [PANDO](https://github.com/kenlabs/pando) that enables easy uploading of all relevant data to substantiate the configuration and performance of SPs operations.

The best source of activity data is metered electricity consumption, electricity utility bills, and reports that document electricity consumption in megawatt-hours (MWh) or kilowatt-hours (kWh). The activity data and information that SPs can submit may include, but is not limited to:&#x20;

* Relevant minerIDs, which we can use to estimate bounds on power use
* Geolocation - approximate Lat / Long coordinates
* Monthly electricity bills
* Granular electricity use measurements, if available
* Documentation of equipment purchases (to substantiate efficiency claims)
* Documentation of renewable energy purchases
* Monthly water bills, or documentation of contract with local water utility/provider
* Documentation of any equipment purchases related to water usage, if applicable
* Photo or video of setup, or video tour with auditor
* An agreement that output data can be made public, or note opting out of some datasets

For metered electricity consumption data, it's worth noting that not all smart meters are created equal. In order for SPs to report energy consumption information from a smart meter for the FCP or their Sustainability Claims, the device must have an error rate of less than 2.5%.

Submitted information will be used for verifying SPs' energy use and hardware performance. Data related to SPs’ specific configurations **will not** be shared publicly. Additional information can be found in the [Filecoin Auditing Process Summary.](https://docs.google.com/document/d/1QTm8Ha2eWsTO2iFX19x98EUjrjTFISZ1uC58yOdDbhQ/edit?usp=sharing)
