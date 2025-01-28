
# test_rave_template

# Create Code Template

## Template Name
```
__test_rave_template
```

## Input Signature

```=json

{
  "type": "object",
  "properties": {
    "test_agent_key": { "type": "string" },
    "amount": { "type": "string" }
  },
  "required": ["test_agent_key", "amount"]
}

```

## Execution Code
```=rhai

const executor_key = "test_executor";
const zero = 0;
if test_agent_key == executor_key {
  return  #{
      "check": true,
      "amount": amount
  };
} else {
  return #{
      "check": false,
      "amount": zero,
  };
}

```

## Output Signature

```=json

{
  "type": "object",
  "properties": {
    "check": { "type": "boolean" },
    "amount": { "type": "string" }
  },
  "required": ["amount"]
}

```
