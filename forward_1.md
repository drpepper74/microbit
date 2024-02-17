# Advanced Agriculture

```package
fwd-edu-breakout=github:climate-action-kits/pxt-fwd-edu/fwd-breakout
ledRing=github:climate-action-kits/pxt-fwd-edu
soilMoisture=github:climate-action-kits/pxt-fwd-edu
```

## Step 7
Click ``||logic: Logic||`` drag and drop ``||logic:If then Else||``
block inside ``||Basic:forever||`` block.
```blocks
basic.forever(function () {
    if (true) {
          }
    else {
        }
        )}
```

## Step 8
Click ``||fwdSensors:Sensors||`` drag and drop ``||fwdSensors:is soilMoisture1 moisture level over 5%||``
to replace ``||logic:true||`` condition of ``||logic:if then else||`` block.
```blocks
basic.forever(function () {
    if (fwdSensors.soilMoisture1.fwdIsMoistureLevelPastThreshold(5, fwdSensors.ThresholdDirection.Over)) {
          }
    else {
        }
        )}
```
