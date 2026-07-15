# Github Access Management
 
## What It Does
 
Users request temporary access to GitHub teams or repositories via an issue. An approver adds the `approved` label, and GitHub Actions automatically grants access. Access expires after the user-specified time.
 
 
## How It Works
 
1. **User** creates an issue using a template (team-based or repo-based).
2. **Approver** reviews the issue and adds the `approved` label.
3. **GitHub Actions** grants access automatically.
4. **Access expires** after the user-defined duration.
5. **Revocation workflow** removes access when expired.
 
---
 
## File Structure
 
```
 
.github/
├── ISSUE_TEMPLATE/
│   ├── access-request-team.yml          # Team access request form
│   └── access-request-repo.yml          # Repo access request form
└── workflows/
├── auto-assign.yml                  # Assigns issue to approvers
├── grant-access.yml                 # Grants access after approval
└── revoke-access.yml                # Revokes expired access daily
 
```
## Complete flow

<img width="1538" height="5388" alt="Media" src="https://github.com/user-attachments/assets/bf41e529-36ff-409a-9f66-bcb839786b00" />
