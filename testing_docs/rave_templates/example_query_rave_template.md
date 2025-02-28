# example_query_rave_template

## Create Code Template

### Template Name

```text
example_query_rave_template
```

## Input Signature

```json
{
  "type": "object",
  "properties": {
    "get_data_for_agent_key": { "type": "any" },
    "unyt_allocation": {
      "type": "array",
      "items": {
        "type": "object",
        "properties": {
          "amount": { "type": "array", "items": { "type": "string" } },
          "agent": { "type": "string" },
          "proof": { "type": "string" }
        },
        "required": ["amount", "agent", "proof"]
      }
    }
  },
  "required": ["get_data_for_agent_key", "unyt_allocation"]
}
```

## Execution Code

```rhai

return #{
  "get_data_for_agent_key": get_data_for_agent_key,
  "unyt_allocation": unyt_allocation
}

```

## Output Signature

```json
{
  "type": "object",
  "properties": {
    "unyt_allocation": {
      "type": "object",
      "properties": {
        "amount": { "type": "array", "items": { "type": "string" } },
        "receiver": { "type": "string" }
      },
      "required": ["amount", "receiver"]
    }
  },
  "required": ["unyt_allocation"]
}
```

## Executable Agreement

// When Creating an (Executable) Agreement for this type of RAVE, these Input Rules are recommended

## Input Rules

```json
[
  {
    "name": "get_data_for_agent_key",
    "instruction": {
      "Query": {
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
    "name": "unyt_allocation",
    "instruction": { "RaveFixed": null }
  }
]
```
