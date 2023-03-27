# CornerAngleRangeArray

Set a group of range to filter the corners by their angles when corners are assembled from line segments.

```json
{
    "CornerAngleRangeArray": 
    [
        {
            "MaxValue" : 110,
            "MinValue" : 70
        }
    ]
}
```

| Key Name | Description | Default Value | Value Range |
| -------- | ----------- | ------------- | ----------- |
| MaxValue | Set the upper limit of the corner angle. | 110 | [0,180] |
| MinValue | Set the lower limit of the corner angle. | 70 | [0,180] |

Be sure that the sum of your MaxValue and MinValue equals to 180. Otherwise, they will be adjusted to fit the requirement.
