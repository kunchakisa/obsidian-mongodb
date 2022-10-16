It stands for **JavaScript Standard Object Notation**. 

## Format

- Start and end with a curly braces `{}`
- Separate each `key` and `value` with a colon `:`
- Separate each `key:value` pair with a comma `,`
- `"keys"` must be surrounded by quotation marks 

## Pros of JSON

- Friendly
- Readable
- Familiar

## Cons of JSON

- Text-based - and text parsing is very slow
- Space-consuming - another concern for databases
- Limited - only supports limited number of data types.
[BSON](BSON.md) aims to alleviate these problems

## Example of JSON

![](assets/20221016193516%20JSON%20Example.png)

## Notes

- Objects inside a JSON object is called a **sub-document** in MongoDB terms.
- Some software (like JavaScript) are **tolerant** to key names without quotation marks. This implementation is **software dependent**. But the actual JSON format **requires** these quotation mark to enclose the key name.

## See Also

- [Field](Field.md), [Value](Value.md)
- [Comparison between JSON and BSON](BSON.md#Comparison%20between%20JSON%20and%20BSON)
- [Comparison Quiz](BSON.md#Quiz)