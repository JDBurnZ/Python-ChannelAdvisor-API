# Python ChannelAdvisor API Example

## Admin Service: Request Access

### Example Request

	from suds.client import Client
	import logging
	
	# Set logging to DEBUG so we can see the outbound and inbound message content.
	logging.basicConfig(level = logging.INFO)
	logging.getLogger('suds.client').setLevel(logging.DEBUG)
	
	# Specify Login Information
	developer_key = 'xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx'
	password = 'xxxxxxxx'
	account_id = 'xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx'

	# Perform the request
	get_order_list = client.factory.create('GetOrderList')
	get_order_list.orderCriteria.OrderCreationFilterBeginTimeGMT = '2000-01-01T00:00:00'
	get_order_list.orderCriteria.OrderCreationFilterEndTimeGMT = '2020-01-01T00:00:00'
	get_order_list.orderCriteria.StatusUpdateFilterBeginTimeGMT = None
	get_order_list.orderCriteria.StatusUpdateFilterEndTimeGMT = None
	get_order_list.orderCriteria.JoinDateFiltersWithOr = None
	get_order_list.orderCriteria.DetailLevel = 'Complete'
	get_order_list.orderCriteria.ExportState = None
	get_order_list.orderCriteria.OrderIDList = None
	get_order_list.orderCriteria.ClientOrderIdentifierList = None
	get_order_list.orderCriteria.OrderStateFilter = 'Active'
	get_order_list.orderCriteria.PaymentStatusFilter = 'Cleared'
	get_order_list.orderCriteria.CheckoutStatusFilter = 'Completed'
	get_order_list.orderCriteria.ShippingStatusFilter = 'Unshipped'
	get_order_list.orderCriteria.RefundStatusFilter = None
	get_order_list.orderCriteria.DistributionCenterCode = None
	get_order_list.orderCriteria.PageSize = 20
	get_order_list.orderCriteria.PageNumberFilter = 1

	more_orders = True
	while more_orders is True:
	        print('Page', get_order_list.orderCriteria.PageNumberFilter)
	        result = client.service.GetOrderList(account_id, get_order_list.orderCriteria)
	
	        if result.ResultData:
	                orders_in_result = len(result.ResultData.OrderResponseItem)
	                print(' Orders In Page:', orders_in_result)
	
	                for order in result.ResultData.OrderResponseItem:
	                        print('         ', order.OrderID)
	
	                if orders_in_result < get_order_list.orderCriteria.PageSize:
	                        more_orders = False
	                else:
	                        get_order_list.orderCriteria.PageNumberFilter += 1
	        else:
	                more_orders = False


### Example Result

	Page 1
		Orders In Page: 20
			 100001
			 100002
			 100003
			 100004
			 100005
			 100006
			 100007
			 100008
			 100009
			 100010
			 100011
			 100012
			 100013
			 100014
			 100015
			 100016
			 100017
			 100018
			 100019
			 100020
	Page 2
		Orders In Page: 3
			100021
			100022
			100023
	All Done!
