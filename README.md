# Device Registry Service

## Usage 

All responses will have the form.

```json
{
	"data": "Mixed type holding the content of the response",
	"message": "Description of what happened."
}
```

Subsequent response definitions will only detail the expected value of the `data fields`.

**Definition** 

`GET /devices`

**Response**

- `200 OK`

```json
	[
		{
			"identifier": "TV",
			"name": "Living Room TV",
			"device_type": "Remote",
			"controller_gateway": "192.168.0.2"
		},
		{
			"identifier": "sdfsfdf",
			"name": "Living Room TV",
			"device_type": "Remote",
			"controller_gateway": "192.168.0.2"
		}
	]
```

### Registering a new device

**Definitions** 

`POST /devices`

**Arguments**

- `"identifier":string` a globally unique identifier for this device.
- `"name":string` a friendly name for this device.
- `"device_type":string` the type of the device as understood by the client.
- `"controller_gateway":string` the IP address of the device's controller. 

