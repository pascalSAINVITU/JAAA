# JAAAWS
Joint Account Autonomoue Agent With Secret for Obyte

# Use cases:
	* Share common funds

# Work flow:
	* One can create a Joint Account including 2 parties (addresses)
	* Any of the 2 parties can send funds
	* Any of the 2 parties can initial a payment
	* The second party receive a message from JAAA to validate the payment
	* The second party validate or cancel the payement
	* If payment validated, then it is executed, if cancel the payment request is delete and the funds stay n the Joint Account
	* At any moment, between the iniatilization and the validation of the payment, any party including the recipient of the payment can cancel the transaction.

# flaw
	The validation request need the user to check, hits history to visit the Unit of the request and retrieve th payment ID.
	
# Possible fields associations

## to setup a Joint Account:
	* account aka ac = <account name> i.e. pascal et simona
	* address1 aka a1 = <address of first party> i.e. HY3PDHJNQNIRTX5NDAYQKY7F3ZQBRQHI
	* address2 aka a2 = <address of second party> i.e. O7NYCFUL5XIJTYE3O4MKGMGMTN6ATQAJ

## to initialize a payment:
	* account aka c = <account name> i.e. pascal et simona
	* amount aka am = <amount> i.e. 3000
	* adrdress aka ad = <recipient address of the payment> i.e. O7NYCFUL5XIJTYE3O4MKGMGMTN6ATQAJ

## to validate a payment:
	this only possible for the parties that are not the initiator of the payment
	* pay_id aka pi = <payment identificator received from JAA> i.e. cjjRlnqJmQY8uIj2rvYBD9NcWvFnnZB6heVCiPy1ZOI=
	
## Cancel a not yet valdiated payment:
	this ossible for any parties including the recipient of the payment
	* pay_id aka pi = <payment identificator received from JAA> i.e. cjjRlnqJmQY8uIj2rvYBD9NcWvFnnZB6heVCiPy1ZOI=
	* cancel aka ca = true
