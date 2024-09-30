# univeralproto

## spec.json5

Where everything comes together.

## types.json5

Defines enums and structure types with a label to be linked in packets.json5.

## packets.json5

Defines messages, their symbol(s), IDs, and links (where necessary) with 
the appropriate payload structure defined in types.json.

This is current packet ID range provisioning:

| Range      | Purpose |
| ---------- | --------|
| `   0- 99` | Sensor readings, command results, or generally anything the firmware reports. |
| ` 100-199` | Commands issued to the boards. |
| ` 200-255` | Reserved. |


## rfc/todo

- Reserving packet ID 100 for handshake requests
- SecondPoint -> SetSecondPoint
- Device specific packets?
- RFC: encode device info into packet ID
  x x x x x x x x
  ^~~~~~~ ^~~~~~~
  class   id

