It stands for **Binary JSON**. It bridges the gap between binary representation and [JSON](JSON.md) format. MongoDB uses

**Optimized for**:
- Speed
- Space
- Flexibility

## Goal

The goal in mind when making BSON was it to be **high performance** and **general purpose**.

## Example of BSON

![](assets/20221016193413%20BSON%20Example.png)

## Comparison between JSON and BSON

- **Encoding** - JSON is encoded with UTF-8 String. BSON is encoded in binary.
- **Data Support** - JSON supports Strings, Booleans, Numbers, Arrays, and sub-objects or sub-documents. BSON supports what JSON supports with additional types for Numbers (Integer, Long, Float, ...), Dates, and Raw Binary.
- **Readability** - JSON is intended to be **Human and Machine readable**, but BSON is optimized for space and sacrifices human readability. BSON is **Machine readable only**.

## Quiz

**Don't scroll too far, or you will see the answer!**

MongoDB stores data in `________`, and you can then view it in `________`.  

`________` is faster to parse and lighter to store than `________`.

`________` supports fewer data types than `________`.

### Answer

MongoDB stores data in **BSON**, and you can then view it in **JSON**.  

**BSON** is faster to parse and lighter to store than **JSON**.

**JSON** supports fewer data types than **BSON**.