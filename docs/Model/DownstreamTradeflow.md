# DownstreamTradeflow

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tradeflow_reference** | **string** | Your unique reference for the tradeflow, for example a purchase order number. |
**container_reference** | [**\Dockflow\Sdk\Model\ContainerReference[]**](ContainerReference.md) | Container numbers (ISO 6346), as a string, an array of strings, or objects with custom properties. | [optional]
**container_references_complete** | **bool** | When true, containers not listed are removed from the tradeflow. When omitted, the list is merged. | [optional]
**bill_of_lading_reference** | [**\Dockflow\Sdk\Model\DownstreamTradeflowBillOfLadingReference**](DownstreamTradeflowBillOfLadingReference.md) |  | [optional]
**bill_of_lading_references_complete** | **bool** | When true, bills of lading not listed are removed. | [optional]
**booking_reference** | [**\Dockflow\Sdk\Model\DownstreamTradeflowBookingReference**](DownstreamTradeflowBookingReference.md) |  | [optional]
**booking_references_complete** | **bool** | When true, bookings not listed are removed. | [optional]
**active** | **bool** | Set to false to deactivate the tradeflow. | [optional]
**carrier_name** | **string** |  | [optional]
**carrier_scac** | **string** | Carrier SCAC. A hint for which carrier to ask first; other carriers are still tried. | [optional]
**customer_name** | **string** | Adds one partner with the role customer. | [optional]
**customer_reference** | **string** |  | [optional]
**partners** | [**\Dockflow\Sdk\Model\DownstreamTradeflowPartnersInner[]**](DownstreamTradeflowPartnersInner.md) |  | [optional]
**partners_complete** | **bool** | When true, partners not listed are removed. | [optional]
**team_name** | **string** | Name of an existing team. Ignored when no team matches. | [optional]
**lead_contact** | **string** | Email or full name of an existing user in your organisation. Ignored when no user matches. | [optional]
**port_of_loading** | **string** | 5-character UN/LOCODE. | [optional]
**port_of_discharge** | **string** | 5-character UN/LOCODE. | [optional]
**estimated_time_of_departure** | **\DateTime** |  | [optional]
**actual_time_of_departure** | **\DateTime** |  | [optional]
**estimated_time_of_arrival** | **\DateTime** |  | [optional]
**actual_time_of_arrival** | **\DateTime** |  | [optional]
**vessel** | **string** |  | [optional]
**incoterms** | **string** |  | [optional]
**references** | [**\Dockflow\Sdk\Model\DownstreamTradeflowReferences**](DownstreamTradeflowReferences.md) |  | [optional]
**events** | [**\Dockflow\Sdk\Model\DownstreamTradeflowEventsInner[]**](DownstreamTradeflowEventsInner.md) | Your own events on the tradeflow. | [optional]
**free_time_overrides** | [**\Dockflow\Sdk\Model\DownstreamTradeflowFreeTimeOverridesInner[]**](DownstreamTradeflowFreeTimeOverridesInner.md) | Free-time overrides, upserted per scope. Unlisted scopes are untouched. | [optional]
**custom_references** | **object** | Flat key-value pairs you define. Values are stored as text; null or an empty string removes the key. | [optional]
**mock_tracking** | [**\Dockflow\Sdk\Model\DownstreamTradeflowMockTracking**](DownstreamTradeflowMockTracking.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
