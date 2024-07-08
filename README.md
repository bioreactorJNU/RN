+----------------+      +----------------+      +----------------+
|     User       |  1   |    Device      |  N   |  SensorData    |
|----------------|------|----------------|------|----------------|
| UserID (PK)    |      | DeviceID (PK)  |      | DataID (PK)    |
| Name           |      | UserID (FK)    |      | DeviceID (FK)  |
| Email          |      | DeviceName     |      | Temperature     |
| Password       |      |                |      | Humidity       |
+----------------+      +----------------+      +----------------+
                                                       |
                                                       |
                                                       |
                                                +----------------+
                                                |   ImageData    |
                                                |----------------|
                                                | ImageID (PK)   |
                                                | DeviceID (FK)  |
                                                | ImageURL       |
                                                | Timestamp      |
                                                +----------------+
