# Dot Notation

**See**: [Source](https://www.mongodb.com/docs/manual/core/document/#dot-notation)

MongoDB uses the _dot notation_ to access the elements of an array and to access the fields of an embedded document.

## Arrays

To specify or access an element of an array by the zero-based index position, concatenate the array name with the dot (`.`) and zero-based index position, and enclose in quotes:

```JSON
"<array>.<index>"
```

For example, given the following field in a document:

```JSON
{
	name: "Alan Turing",
	birthday: ...,
	...
	contribs: [ "Turing machine", "Turing test", "Turingery" ],
	...
}
```

To specify the third element in the `contribs` array, use the dot notation `"contribs.2"`.

## Sub-Documents

To specify or access a field of an embedded document with dot notation, concatenate the embedded document name with the dot (`.`) and the field name, and enclose in quotes:

```JSON
"<embedded document>.<field>"
```

For example, given the following field in a document:

```JSON
{
	...
	name: { first: "Alan", last: "Turing" },
	contact: { phone: { type: "cell", number: "111-222-3333" } },
	...
}
```

-   To specify the field with value `"Turing"` in the `name` field, use the dot notation `"name.last"`.
-   To point to the value `111-222-3333` in the `phone` document in the `contact` field, use the dot notation `"contact.phone.number"`.