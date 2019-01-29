# pydcm

```python
from pydcm import dcminfo

dcm = dcminfo()
dcm.read("../data/DEMO.DCM")
# find functions:0, calibrations:5, axises:0

DEMO_CURVE = dcm.calibrations["DEMO_CURVE"]
print(DEMO_CURVE)
# name=DEMO_CURVE, description=This is a standard curve: one input and one output.
# line_start=35, line_end=43
# type=CURVE, unit=
# value=
# [0.30078125, 0.3984375, 0.5, 0.59765625, 0.69921875, 0.80078125, 0.8984375]
# axis x
# name=, description=
# line_start=0, line_end=0
# type=, unit=revs
# value=
# [120.0, 200.0, 320.0, 400.0, 520.0, 600.0, 720.0]

DEMO_MAP_2 = dcm.getcalobject("calibration", "DEMO_MAP_2")
DEMO_MAP_2.show()
```

![image](/image/DEMO_MAP_2.png)

# English

dcm(Data Conservation Format) is a calibration data format, it's extension is .dcm. INCA, CANape and other calibration tool support this. 

This repro is a dcm library in python, which is used for read and write dcm file.

#  中文

dcm（Data Conservation Format）是一种标定数据格式，后缀是.dcm，INCA/CANape等标定工具都支持。

本项目是使用python开发的dcm库，用于读写dcm。