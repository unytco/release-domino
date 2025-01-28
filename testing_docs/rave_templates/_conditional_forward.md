# _conditional_forward

# Create Code Template

## Template Name
```
__conditional_forward
```

## Input Signature

```=json

{
  "type": "object",
  "properties": {
    "amount": { "type": "string" }
  },
  "required": ["amount"]
}

```

## Execution Code
```=rhai

return #{
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
    name: "amount",
    instruction: { RaveFixed: null },
}
```
