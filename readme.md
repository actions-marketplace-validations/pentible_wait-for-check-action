# wait-for-check-action

## Usage

<!-- prettier-ignore -->
```yaml
steps:
  - name: Wait for CI
    id: wait-ci
    uses: pentible/wait-for-check-action@v1
    with:
      # ie. if check comes from a github action, it will be the job name
      check-name: ci
  - name: Print Conclusion
    run: echo "${{ steps.wait-ci.outputs.conclusion }}"
```

## Local dev

-   `./bin/dev initial setup`
-   run the following commands AND append to your shell configs (ie. `~/.zshrc`
    or `~/.bashrc`/`~/.bash_profile`)

```bash
eval "$(mise activate zsh)"
# or for bash
# eval "$(mise activate bash)"
```

-   (optionally) configure mise: `~/.config/mise/settings.toml`

```toml
trusted_config_paths = ["~/Projects"] # where ~/Projects is wherever you clone your repos
```

-   `dev start`