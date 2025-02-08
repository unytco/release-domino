# \_\_system_credit_limit_computation

# Create Code Template

## Template Name

```
__system_credit_limit_computation
```

## Input Signature

```json
{
  "type": "object",
  "properties": {
    "special_account_pubkey": { "type": "string" },
    "claiming_agent_pubkey": { "type": "string" },
    "special_account_credit_limit": { "type": "string" }
  },
  "required": ["special_account_pubkey", "claiming_agent_pubkey", "special_account_credit_limit"]
}
```

## Execution Code

```rhai

///  Fixed amounts for Infra/Unyt and service network ops/admins

if claiming_agent_pubkey == special_account_pubkey {
  return  #{
      "credit_limit": [
        #{
            "agent": special_account_pubkey,
            "amount": special_account_credit_limit
        }
      ]
  };
} else {
  return #{
      "credit_limit": [
        #{
            "agent": claiming_agent_pubkey,
            "amount": "100"
        }
      ]
  };
}

```

## Output Signature

```json
{
  "type": "object",
  "properties": {
    "credit_limit": {
      "type": "array",
      "items": {
        "type": "object",
        "properties": { "agent": { "type": "string" }, "amount": { "type": "string" } },
        "required": ["agent", "amount"]
      }
    }
  },
  "required": ["credit_limit"]
}
```

# Executable Agreement

// When Creating an (Executable) Agreement for this type of RAVE, these Input Rules are recommended

## Input Rules

- `special_account_pubkey`: `Fixed` // add the pubkey of the agent that will serve as the infrastructure account (can be your pubkey)
- `claiming_agent_pubkey`: `ExecutorProvided`
- `special_account_credit_limit`: `Fixed` // type in the number of credits that the infrastructure account will be allowed to go into the negative. ex: 10,000
