# test_query_rave_template

# Create Code Template

## Template Name
```
__test_query_rave_template
```

## Input Signature

```=json

{
  "type": "object",
  "properties": {
    "get_data_for_agent_key": { "type": "any" },
    "amount": { "type": "string" }
  },
  "required": ["get_data_for_agent_key", "amount"]
}

```

## Execution Code
```=rhai

return #{
  "get_data_for_agent_key": get_data_for_agent_key,
  "amount": amount
}

```


## Output Signature

```=json

{
  "type": "object",
  "properties": {
    "amount": { "type": "string" }
  },
  "required": ["amount"]
}

```

# Executable Agreement
// When Creating an (Executable) Agreement for this type of RAVE, these Input Rules are recommended

## Input Rules

```json=
{
    name: "get_data_for_agent_key",
    instruction: {
        Query: {
            "GetAgentActivity": [
                "uhCAkdqEGyaphIqtBSW9Bu19Ixxlvj5CwO3mkCmBmF6xZCSwqhPw1",
                {
                    "sequence_range": "Unbounded",
                    "entry_type": null,
                    "entry_hashes": null,
                    "action_type": null,
                    "include_entries": true,
                    "order_descending": true
                },
                { "Full": null }
            ]
        }
    }
},
{
    name: "amount",
    instruction: { RaveFixed: null },
}
```
