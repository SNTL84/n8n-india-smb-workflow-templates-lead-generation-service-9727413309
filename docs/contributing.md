# Contributing to n8n India SMB Workflow Templates

Thank you for wanting to contribute! This repo grows through community submissions.

## What Makes a Good Template

- **India-specific**: Uses Indian payment gateways, logistics, or communication tools
- **Solves a real problem**: A workflow someone actually uses, not a demo
- **Ready to import**: Working JSON that can be imported into n8n without errors
- **Well-documented**: Clear description, required credentials listed, setup instructions

## How to Submit

1. **Fork** this repo
2. Create a new branch: `git checkout -b add-your-workflow-name`
3. Add your workflow JSON to `workflows/your-workflow-name.json`
4. Add a row to the relevant table in `README.md`
5. If setup needs explanation, add a doc to `docs/`
6. Submit a **Pull Request** with a short description of what it does

## JSON Template Format

Your workflow JSON should include:
- `name`: Human-readable name
- `nodes`: Array of n8n nodes
- `connections`: Node connection map
- `meta.description`: What it does, what credentials are needed, what to replace

## Code of Conduct

- Be kind and constructive
- Test your workflow before submitting
- No proprietary credentials in the JSON — use placeholder values like `YOUR_API_KEY`

---
*Questions? Reach out: [WhatsApp](https://wa.me/919727413309) · [desidevloper.com](https://desidevloper.com)*
