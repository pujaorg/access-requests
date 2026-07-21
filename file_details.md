## 🏷️ Label Conflict Resolution yml file

The `label-conflict.yml` workflow ensures that only **one status label** can be active on an issue at a time, preventing conflicts.

### 🎯 Purpose

- Prevents `approved` from coexisting with `denied` or `needs-info`
- Blocks adding `denied` or `needs-info` when `approved` is present
- Allows `denied` and `needs-info` to coexist

### 📋 Behavior

| Label Added | If `approved` is present | If `approved` is NOT present |
| :--- | :--- | :--- |
| `approved` | ✅ `denied` and `needs-info` are removed | ✅ `approved` added |
| `denied` | ❌ `denied` is removed (blocked) | ✅ `denied` added |
| `needs-info` | ❌ `needs-info` is removed (blocked) | ✅ `needs-info` added |

### ✅ Allowed Combinations

| Labels | Allowed? |
| :--- | :--- |
| `approved` only | ✅ Yes |
| `denied` only | ✅ Yes |
| `needs-info` only | ✅ Yes |
| `denied` + `needs-info` | ✅ Yes |
| `approved` + `denied` | ❌ No |
| `approved` + `needs-info` | ❌ No |
| `approved` + `denied` + `needs-info` | ❌ No |

> **Note:** This workflow runs automatically whenever a label is added to an issue.
