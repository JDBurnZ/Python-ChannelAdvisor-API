# Python-ChannelAdvisor-API
Examples interfacing with ChannelAdvisor API Services in Python 3

## Prerequisites

Python 3: https://www.python.org/downloads/

A Python 3 port of suds available through pypi at https://pypi.python.org/pypi/suds-jurko or by running the following command in your terminal:

	$ sudo pip3 install suds-jurko

## Examples

### Admin Service
<ul>
<li>GetAuthorizationList</li>
<li><a href="AdminService-RequestAccess.md">RequestAccess</a></li>
<li><a href="AdminService-Ping.md">Ping</a></li>
</ul>

### Cart Service
<ul>
<li>CreateCart</li>
<li>GetCart</li>
<li>DeleteCart</li>
<li>ModifyCart</li>
<li>Ping</li>
</ul>

### Fulfillment Service
<ul>
<li>CreateOrderFulfillments</li>
<li>GetOrderFulfillmentDetailList</li>
<li>MoveFulfillmentItems</li>
<li>UpdateOrderFulfillments</li>
</ul>

### Inventory Service
<ul>
<li>AddUpsellRelationship</li>
<li>AssignLabelListToInventoryItemList</li>
<li>DeleteInventoryItem</li>
<li>DeleteUpsellRelationship</li>
<li>DoesSkuExist</li>
<li>DoesSkuExistList</li>
<li>GetClassificationConfigurationInformation</li>
<li>GetDistributionCenterList</li>
<li>GetFilteredInventoryItemList</li>
<li>GetFilteredSkuList</li>
<li>GetInventoryItemAttributeList</li>
<li>GetInventoryItemList</li>
<li>GetInventoryItemQuantityInfo</li>
<li>GetInventoryItemStoreInfo</li>
<li>GetInventoryItemImageList</li>
<li>GetInventoryItemShippingInfo</li>
<li>GetInventoryItemVariationInfo</li>
<li>GetInventoryQuantity</li>
<li>GetInventoryQuantityList</li>
<li>GetUpsellRelationship</li>
<li>Ping</li>
<li>RemoveLabelListFromInventoryItemList</li>
<li>SynchInventoryItem</li>
<li>SynchInventoryItemList</li>
<li>UpdateInventoryItemQuantityAndPrice</li>
<li>UpdateInventoryItemQuantityAndPriceList</li>
</ul>

### Listing Service
<ul>
<li>WithdrawListings</li>
</ul>

### Market Ad Service
<ul>
<li>AddMarketplaceAd</li>
<li>AddMarketplaceAdForSkuList</li>
<li>DeleteMarketplaceAd</li>
</ul>

### Order Service
<ul>
<li>GetOrderList</li>
<li>GetOrderRefundHistory</li>
<li><a href="OrderService-Ping.md">Ping</a></li>
<li>OrderMerge</li>
<li>OrderSplit</li>
<li>SubmitOrder</li>
<li>SubmitOrderRefund</li>
<li>SetOrdersExportStatus</li>
<li>SetSellerOrderID</li>
<li>SetSellerOrderItemIDList</li>
<li>UpdateOrderList</li>
</ul>

### Shipping Service
<ul>
<li>Ping</li>
<li>GetOrderShipmentHistoryList</li>
<li>GetShippingRateList</li>
<li>GetShippingCarrierList</li>
<li>SubmitOrderShipmentList</li>
</ul>

### Store Service
<ul>
<li>Ping</li>
<li>GetSearchAnalysisStats</li>
</ul>
