AWS Region

## About
- Regions are made up of multiple [[Availability Zone]]s.
- A Region is comprised of at least 2 AZs.

### Factors to Consider When Selecting a Region
1. Compliance with data governance and legal requirements
	1. You may need to run your data out of specific locations. If your company requires all your data to reside in the UK, you would choose the London Region.
2. Proximity to your customers
	1. Ex: Your company is based in Washington DC, and your customers live in Singapore. Your might want to run your infrastructure in the Northern Virginia Region (close to your headquarters), but run the application from the Singapore Region.
3. Available services within a Region
	1. AWS is frequently making new services available, but sometimes this requires AWS to build out the hardware one Region at a time.
	2. Some Regions may be able to run new services that other Regions cannot.
4. Pricing
	1. Pricing is dependent on countries' tax structures (and I assume other factors too). The cost of services can vary widely across Regions.
