# Python ChannelAdvisor API Example

## Admin Service: Ping

### Example Request
	from suds.client import Client
	import logging

	# Set logging to DEBUG so we can see the outbound and inbound message content.
	logging.basicConfig(level = logging.INFO)
	logging.getLogger('suds.client').setLevel(logging.DEBUG)

	# Specify Login Information
	developer_key = 'xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx'
	password = 'xxxxxxxx'

	# Specify URLs
	wsdl_url = 'https://api.channeladvisor.com/ChannelAdvisorAPI/v7/AdminService.asmx?WSDL'
	service_url = 'https://api.channeladvisor.com/ChannelAdvisorAPI/v7/AdminService.asmx'

	# Initialize client.
	client = Client(wsdl_url, location = service_url)

	# Pass login information
	login = client.factory.create('APICredentials')
	login.DeveloperKey = developer_key
		login.Password = password
	client.set_options(soapheaders=login)

	# Perform the request
	response = client.service.Ping()

	# Print response
	print(response)

### Example Response

	(APIResultOfString){
	  Status = "Success"
	  MessageCode = 0
	  ResultData = "OK"
	}
