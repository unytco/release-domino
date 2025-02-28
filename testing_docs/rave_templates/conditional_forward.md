# conditional_forward

## Create Code Template

### Template Name

```text
conditional_forward
```

## Input Signature

```json
{
  "type": "object",
  "properties": {
    "unyt_allocation": {
      "type": "object",
      "properties": {
        "amount": { "type": "array", "items": { "type": "string" } },
        "agent": { "type": "string" },
        "proof": { "type": "string" }
      },
      "required": ["amount", "agent", "proof"]
    }
  },
  "required": ["unyt_allocation"]
}
```

## Execution Code

```rhai

return #{
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
        "agent": { "type": "string" }
      },
      "required": ["amount", "agent"]
    }
  },
  "required": ["unyt_allocation"]
}
```

## Executable Agreement

// When Creating an (Executable) Agreement for this type of RAVE, these Input Rules are recommended

## Input Rules

```json
{
  "name": "unyt_allocation",
  "instruction": { "RaveFixed": null }
}
```
