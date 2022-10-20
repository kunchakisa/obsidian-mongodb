- An `ObjectId` consists of 12 bytes. It is divided to:
	- A 4-byte timestamp, representing the ObjectId's creation time, measured in seconds since the [Unix epoch](Unix%20Epoch.md).
	- A 5-byte random value generated once per process. This random value is unique to the machine and process.
	- A 3-byte incrementing counter, initialized to a random value.
- A sample is `ObjectId("507f1f77bcf86cd799439011")`.
- Let's divide the hexadecimal string to bytes. (A byte is represented by 2 hexadecimal digits). `507f1f77-bcf86cd799-439011`. We can see here the parts of the 12-byte `ObjectId`.
- Note that since the middle portion of the `ObjectId` is a random value generated per process, you'll see in the database the same middle part if they are inserted with the same process.
![](assets/20221017093052%20ObjectId%20samples.png)
- In the picture, the 1st part of the `ObjectId` is the same because they are sample datasets and they are all made in the same second, leaving the Unix timestamp unchanged.