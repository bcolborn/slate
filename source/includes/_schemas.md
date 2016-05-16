# Schemas

## Create network request
<table>
	<tr>
		<th>Description</th>
		<td>Request to make a network</td>
	</tr>
	<tr>
		<th>Name</th>
		<td>network</td>
	</tr>
	<tr>
		<th>Type</th>
		<td>object</td>
	</tr>
</table>

### Properties
| Property | Type | Required?
| -------- | ---- | ---------
| api_version | string | *
| metadata | #/definitions/network_metadata | *
| spec | #/definitions/network_resources | 
| status | #/definitions/network_resources | 

## Response Kind
<table>
	<tr>
		<th>Description</th>
		<td>The status of a REST API call. Only used when there is a failure to report.</td>
	</tr>
	<tr>
		<th>Name</th>
		<td>network_status</td>
	</tr>
	<tr>
		<th>Type</th>
		<td>object</td>
	</tr>
</table>

### Properties
| Property | Description | Type | Default | Read only?
| -------- | ----------- | ---- | ------- | ----------
| api_version | | string | | *
| code | The HTTP error code | integer | | *
| details | Custom key-value details relevant to the status | object (string) | | *
| kind | The kind name | string | network | *
| message | A sentence explaining the reason for the status | string | | *
| reason | One snake_case word | string | | *
| status | Only value possible is "failure" | string | | *

## Network metadata
<table>
	<tr>
		<th>Description</th>
		<td>The network kind metadata</td>
	</tr>
	<tr>
		<th>Name</th>
		<td>network_metadata</td>
	</tr>
	<tr>
		<th>Type</th>
		<td>object</td>
	</tr>
</table>

### Properties

| Property | Description | Type | Default | Read only?
| -------- | ----------- | ---- | ------- | ----------
| last_update_time | Time when network was last updated | string | | *
| kind | The kind name | string | network | *
| uuid | network uuid| string | 
| creation_time | Time when network was created | string |
| account_reference | See schema definition | #/definitions/account_reference
| owner_reference | See schema definition | #/definitions/user_reference
| entity_version | Monotonically increasing number | integer
| name | network name | string

# Patterns

UUID: ^[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}$