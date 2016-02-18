# pilatus-1.0

A __pilatus-1.0__ message consists of two sub-messages, the main header and a binary part which holds the raw bytes of the cbf files "written" by the (Pilatus) detector.

```
[[main header][binary blob cbf]]
```

The header consists of following fields:


| Name | Type | Default | Comment |
| ---- | ---- | --------| ------- |
| htype | String | pilatus-1.0 | htype of header |
| filename | String | "" | Name of the cbf file written by the camserver software |
| path | String | "" | relative path for the location of the file |
