# chunk-1.0
__deprecated use array-1.0 instead__

chunk-1.0 specifies the header of image chunks from a camera/detector source like PCO Edge or Eiger.

| Name | Type | Default | Comment |
| ---- | ---- | ------- | ------- |
| shape | Array[ Integer ] | [] | [x,y,z,...] |
| type | String | | (u)int8, (u)int16, (u)int32, (u)int64, float16, float32, float64 |
| cmpr | String | "" | byte shuffling, nbit filter and compression algorithm __\[s-&#124;n\[BIT]-]__(zlib\[LVL], lz4, lzf, cbf) BIT= number 1,2,4,8: numbers of bits in nbit filter LVL= 0-9: compression level for zlib. For no compression omit the *cmpr* attribute.
| frame | Integer | | Frame ID starting at 0 |

The default byte order is little-endian.

## Examples cmpr
* Byte shuffling + lz4 compressiong = s-lz4
* nbit filter (8 bits) + lz4 compression = n8-lz4
