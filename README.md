# action-dotnet-format
dotnet-format for GitHub Actions

## Usage

See [action.yml](action.yml)

**Basic**:
```yaml
steps:
  - uses: actions/checkout@v4
  - uses: actions/setup-dotnet@v4
    with:
      dotnet-version: '8.0.x'
  - uses: tsubakimoto/action-dotnet-format@v0
    with:
      base-branch: ${{ github.head_ref }}
      project-path: 'example.csproj'
      github-token: ${{ secrets.GITHUB_TOKEN }}
```

### Permissions

The `GITHUB_TOKEN` secret is required to create a pull request.

| Permission | Value |
| --- | --- |
| `contents` | `write` |
| `pull_requests` | `write` |

## License

The scripts and documentation in this project are released under the [MIT License](LICENSE)
