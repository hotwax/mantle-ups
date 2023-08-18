# mantle-ups
Ups shipping gateway integration

Integration with UPS for shipping rates, labels, and create orders. In this Integration we worked on staging environment. So, the rates may vary from production evironment.

To use simply:

Load the setup data in data/UpsSetupData.xml
Load the demo configuration data in data/UpsZaaDemoData.xml or create your own configuration and load it; if you use the demo data, add your API credentials (SgoUPSUsername, SgoUPSPassword and SgoUPSShipperNumber).

~ get#ShippingRates service: 
This Rate API will return a rate as per the destination location and parcel attributes. At minimum, a Rating API requires a Shipper and ShipTo information. However, different couriers and delivery methods can require additional fields to satisfy their requirements.

~ create#ShippingLabel service : 
This label API will return a URL to a label for an order. Retrieves labelling information for an Order using the tracking number.

~ void#ShippingLabel service: 
The Void Shipping API is used to cancel the previously scheduled shipment. The API first checks if the Shipment can be cancelled, ie., if its current state allows it, then returns an immediate response. If the Shipment is successfully cancelled, the API will answer with the Shipment with its state updated as cancelled.
