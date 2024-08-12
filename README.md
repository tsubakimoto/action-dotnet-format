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
  - uses: tsubakimoto/action-dotnet-format@v1
    with:
      base-branch: ${{ github.ref_name }}
      project-path: 'example.csproj'
      verbosity: 'diag'
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
