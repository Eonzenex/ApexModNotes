Just Cause 4 uses an updated version of Runtime Property Container (RTPC) version 3. The structure of the RTPC has been flattened, and all properties, not just strings, are checked for uniqueness and stored in blocks together.
# Structure
## RTPC file header
| Name | Type | Notes |
| ---- | ---- | ---- |
| Magic | UTF-8 | Set to RTPC |
| Version | uint32 | Set to 3 |
## Container
### Container header
| Name | Type |
| ---- | ---- |
| Hash | uint32 |
| Offset | uint32 |
| Property count | uint16 |
| Container count | uint16 |
### Container body
| Name | Type |
| ---- | ---- |
| Properties | [[Runtime Property Container (RTPC)#Property header\|Property header]][] |
| Container headers | [[Runtime Property Container (RTPC)#Container header\|Container headers]][] |
| Valid/assigned property count | uint32 |
| Container bodies | [[Runtime Property Container (RTPC)#Container body\|Container body]][] |
## Property
### Property header
| Name | Type |
| ---- | ---- |
| Name hash | uint32 |
| Data | uint32 |
| Variant | [[Runtime Property Container (RTPC)#Property variant\|Property variant]] |
### Property variant
#### Unassigned
**Value:** 0x00
**Alignment:** 0
**Notes:** Primitive
#### UInt32
**Value:** 0x01
**Alignment:** 0
**Notes:** Primitive
#### Float
**Value:** 0x02
**Alignment:** 0
**Notes:** Primitive
#### String
**Value:** 0x03
**Alignment:** 0
#### Vector 2
**Value:** 0x04
**Alignment:** 4
#### Vector 3
**Value:** 0x05
**Alignment:** 4
#### Vector 4
**Value:** 0x06
**Alignment:** 16
#### Matrix 3x3
**Value:** 0x07
**Alignment:** 4
#### Matrix 4x4
**Value:** 0x08
**Alignment:** 16
#### UInt32 array
**Value:** 0x09
**Alignment:** 4
#### Float array
**Value:** 0x0A
**Alignment:** 4
#### Byte array
**Value:** 0x0B
**Alignment:** 16
#### Unknown 01/deprecated
**Value:** 0x0C
**Alignment:** 4
#### Object ID
**Value:** 0x0D
**Alignment:** 4
#### Event array
**Value:** 0x0E
**Alignment:** 4
#### Total
**Value:** 0x0F
**Alignment:** 4
