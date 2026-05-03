# Contributing to nullapt/skills

Thanks for adding a skill to the community index!

## Steps

1. Fork and clone this repo
2. Create `skills/<skill-name>/index.json` using the schema in the README
3. Run the linter: `npx ajv validate -s schema/index.schema.json -d skills/<skill-name>/index.json`
4. Open a PR with the title `feat(skill): add <skill-name>`

## Review process

- CI checks JSON schema validity and that the `registry_url` resolves
- Maintainers verify permissions are accurately disclosed
- Merge typically within 48 hours for simple skills
