# example_rave_template

## Create Code Template

### Template Name

```text
example_rave_template
```

## Input Signature

```json
{
  "type": "object",
  "properties": {
    "test_agent_key": { "type": "string" },
    "invalid_agent_key": { "type": "string" },
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
  "required": ["test_agent_key", "unyt_allocation"]
}
```

## Execution Code

```rhai

const zero = 0;
// iterate over unyt_allocation and return 0 if the test_agent_key is the invalid_agent_key
for i in 0..unyt_allocation.len {
  if unyt_allocation[i].agent == invalid_agent_key {
    unyt_allocation[i].amount = zero;
  }
}
return  #{
    "unyt_allocation": unyt_allocation
};

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
    "name": "test_agent_key",
    "instruction": { "ExecutorProvided": null }
  },
  {
    "name": "invalid_agent_key",
    "instruction": { "Fixed": "uhCAkdqEGyaphIqtBSW9Bu19Ixxlvj5CwO3mkCmBmF6xZCSwqhPw1" }
  },
  {
    "name": "unyt_allocation",
    "instruction": { "RaveFixed": null }
  }
]
```
