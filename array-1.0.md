# array-1.0

__array-1.0__ specifies the header of image messages from a camera/detector source like PCO Edge or Eiger.

| Name | Type | Default | Comment |
| ---- | ---- | ------- | ------- |
| shape | Array[ Integer ] | [] | [...,z,y,x] |
| type | String | | (u)int8, (u)int16, (u)int32, (u)int64, float16, float32, float64 |
| endianness | String | "little" | big, little |
| frame | Integer | | Frame ID starting at 0 |
| source | String | "" | Used to identify hardware source |
| encoding | String | "" | Used to identify e.g. whether data is compressed, etc.|

# Examples
* Minimal Header
```json
{"htype":"array-1.0", "shape":[10,20], "type":"uint16", "frame":0}
```
* PCO Edge
```json
{"htype":"array-1.0", "tags":[], "source":"", "shape":[2160,2560], "frame":434, "type":"uint16", "endianess":"little"}
```
