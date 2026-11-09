# DocumentUpload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tradeflow_reference** | **string** | The tradeflow to attach the document to. |
**document_extension** | **string** |  |
**document_payload_base64** | **string** | The file contents, base64-encoded. |
**document_type** | **string** | A type name from GET /v3/downstream/documents/types. Unknown or omitted: no type. | [optional]
**document_filename** | **string** | File name without extension, shown in Dockflow. | [optional]
**container_reference** | **string** | Links the document to one container of the tradeflow. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
