# ct-templates-index

Community template index for [ct-cli](https://github.com/jean3690/ct-cli) — browse and search code templates.

## Usage

```bash
# Search templates from the index
ct-cli template search web
ct-cli template search go
ct-cli template search --lang rust

# Import a template from the index
ct-cli template import --git <url> <name>
```

## Submitting a template

1. Fork this repository
2. Add your template entry to `index.yaml`
3. Open a pull request

### Entry format

```yaml
- name: my-template
  description: "Short description of what it generates"
  languages: [go, python]
  url: https://github.com/your-username/your-template-repo
  version: "1.0.0"
  author: your-username
  tags: [cli, web, api]
```

### Requirements for template repos

- Must have a valid `manifest.yaml` at the repo root
- Must be a public repository
- Follow [ct-cli template authoring guide](https://github.com/jean3690/ct-cli#template-authoring)

## Schema

| Field | Required | Description |
|---|---|---|
| `name` | yes | Unique template name (used with `ct-cli new <name>`) |
| `description` | yes | What this template generates |
| `languages` | yes | Programming language(s) |
| `url` | yes | Git repository URL |
| `version` | no | Latest version |
| `author` | no | Author name/handle |
| `tags` | no | Search keywords |

## License

MIT
