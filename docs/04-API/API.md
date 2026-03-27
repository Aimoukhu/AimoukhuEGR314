---
title: API
---

The IMU subsystem can transmit information such as orientation (yaw, pitch, and roll), acceleration data, calibration status, and sensor errors. These messages allow other subsystems to monitor system movement, determine heading, and verify that the sensor is operating correctly.

> All messages from this subsystem are sent to and from the hub.

## Subsystem Unique ID

| Individual | No. |
|:----------:|:---:|
|   Sam B    |  1  |
|  Adrian P  |  2  |
|  Andrew I  |  3  |
|  Jacob D   |  4  |
|   Sam M    |  5  |
|    Mo A    |  6  |

## IMU Subsystem Downstream Requests

**Message Type 2 -- Request Motor Speed**

|               |    Byte 1    |      Byte 2      |    Byte 3    |      Byte 4       |      Byte 5       |     Byte 6      |
|:-------------:|:------------:|:----------------:|:------------:|:-----------------:|:-----------------:|:---------------:|
| Variable Name | Message_Type | Subsystem_Number | Motor_Number | Upper Motor_Speed | Lower Motor_Speed | Motor_Direction |
| Variable Type |   uint8_t    |     uint8_t      |   uint8_t    |      uint8_t      |      uint8_t      |     uint8_t     |
|   Min Value   |      2       |        3         |      0       |         0         |         0         |        0        |
|   Max Value   |      2       |        3         |      1       |        15         |        15         |        1        |
|    Example    |      2       |        3         |      1       |         4         |         4         |        1        |

**Message Type 3 -- Request Rover Orientation**

|               |    Byte 1    |      Byte 2      |  Byte 3   |  Byte 4   |   Byte 5    |   Byte 6    |   Byte 7   |   Byte 8   |
|:-------------:|:------------:|:----------------:|:---------:|:---------:|:-----------:|:-----------:|:----------:|:----------:|
| Variable Name | Message_Type | Subsystem_Number | yaw_upper | yaw_lower | pitch_upper | pitch_lower | roll_upper | roll_lower |
| Variable Type |   uint8_t    |     uint8_t      |  int8_t   |  int8_t   |   int8_t    |   int8_t    |   int8_t   |   int8_t   |
|   Min Value   |      3       |        3         |    -90    |    -90    |     -90     |     -90     |    -180    |    -180    |
|   Max Value   |      3       |        3         |    225    |    90     |     90      |     90      |    180     |    180     |
|    Example    |      3       |        3         |     4     |     4     |      8      |      0      |     9      |      1     |

**Message Type 13 -- Request Subsystem Status**

|               |    Byte 1    |      Byte 2      | 
|:-------------:|:------------:|:----------------:|
| Variable Name | message_type | subsystem_Number | 
| Variable Type |   uint8_t    |     uint8_t      |
|   Min Value   |      13      |        3         |    
|   Max Value   |      13      |        3         | 
|    Example    |      13      |        3         |  


## IMU Subsystem Upstream Request

**Message Type 14 - Subsystem Error Response**

|               |    Byte 1    |    Byte 2     |    Byte 3    |    Byte 4    |    Byte 5    |
|:-------------:|:------------:|:-------------:|:------------:|:------------:|:------------:|
| Variable Name | message_type | Source_Number | Upper_Number | Lower_Number | Description  |
| Variable Type |   uint8_t    |    uint8_t    |    int8_t    |   uint8_t    |    Char[]    |
|   Min Value   |      14      |       3       |      0       |      0       |     Null     |
|   Max Value   |      14      |       3       |      10      |      10      | Byte 8 - 61  |
|    Example    |      14      |       3       |      1       |      4       | Not Detected |

**Message Type 15 - Subsystem Status Response**

|               |    Byte 1    |    Byte 2     |    Byte 3    |    Byte 4    |    Byte 5    |
|:-------------:|:------------:|:-------------:|:------------:|:------------:|:------------:|
| Variable Name | message_type | Source_Number | Upper_Number | Lower_Number | Description  |
| Variable Type |   uint8_t    |    uint8_t    |    int8_t    |   uint8_t    |    Char[]    |
|   Min Value   |      14      |       3       |      0       |      0       |     Null     |
|   Max Value   |      14      |       3       |      10      |      10      | Byte 8 - 61  |
|    Example    |      14      |       3       |      1       |      8       | Calibrating |
