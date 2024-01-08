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
| ID/Name | uint32 |
| Offset | uint32 |
| Property count | uint16 |
| Container count | uint16 |
### Container body
| Name | Type |
| ---- | ---- |
| Properties | [[Runtime Property Container (RTPC)#Property header\|Property header]][] |
| Container headers | [[Runtime Property Container (RTPC)#Container header\|Container headers]][] |
| Valid/assigned property count | uint32 |
## Property
### Property header
| Name | Type |
| ---- | ---- |
| Name hash | uint32 |
| Data | uint32 |
| Variant | [[Runtime Property Container (RTPC)#Property variant\|Property variant]] |
### Property variant
#### Unassigned
**Value:** 0
**Alignment:** 0
**Notes:** Primitive
#### UInt32
**Value:** 1
**Alignment:** 0
**Notes:** Primitive
#### Float
**Value:** 2
**Alignment:** 0
**Notes:** Primitive
#### String
**Value:** 3
**Alignment:** 0
#### Vector 2
**Value:** 4
**Alignment:** 4
#### Vector 3
**Value:** 5
**Alignment:** 4
#### Vector 4
**Value:** 6
**Alignment:** 16
#### Matrix 3x3
**Value:** 7
**Alignment:** 4
#### Matrix 4x4
**Value:** 8
**Alignment:** 16
#### UInt32 array
**Value:** 9
**Alignment:** 4
#### Float array
**Value:** A
**Alignment:** 4
#### Byte array
**Value:** B
**Alignment:** 16
#### Unknown 01/deprecated
**Value:** C
**Alignment:** 4
#### Object ID
**Value:** D
**Alignment:** 4
#### Event array
**Value:** E
**Alignment:** 4
#### Total
**Value:** F
**Alignment:** 4
