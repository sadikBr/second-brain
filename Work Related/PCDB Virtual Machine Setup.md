1. Deploy Manufacturer changes.
	1. Load the new manufacturer global attributes `windchill wt.load.LoadFromFile -u wcadmin -p wcadmin -d loadFiles.custo\iba\PCDB_UpdateAdminObjects.xml -CONT_PATH wt.inf.container.OrgContainer=PCDB`
	2. Load the new manufacturer soft attributes `windchill wt.load.LoadFromFile -u wcadmin -p wcadmin -d loadFiles.custo\type\PCDB_UpdateManufacturerType.xml -CONT_PATH wt.inf.container.OrgContainer=PCDB`

2. Deploy the new SubContractor type.
	1. Load the SubContractor global attributes.
	2. Load the SubContractor type.
	3. Load the SubContractor lifecycle.
	4. Load the SubContractor InitRule.

3. Deploy the link between the SubContractor type and Sources.
	1. Load the SubContractorSouce link.