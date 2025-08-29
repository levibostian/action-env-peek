# Environment Peek Action

A very simple GitHub composite action that prints environment and context information to the CI logs for debugging purposes.

## What it does

This action performs three debugging tasks:

1. **Debug GitHub Event**: Prints the contents of `$GITHUB_EVENT_PATH` (the webhook payload that triggered the workflow) in formatted JSON
2. **Debug GitHub Context**: Prints the GitHub context object with all its properties in formatted JSON  
3. **Debug Environment Variables**: Lists all environment variables in alphabetical order

## Usage

Add this step to your workflow:

```yaml
- name: Debug Environment
  uses: levibostian/action-env-peek@main
```

## Output

The action will output three sections in your CI logs:

1. **GitHub Event Data**: Complete webhook payload
2. **GitHub Context**: All GitHub-specific context variables
3. **Environment Variables**: All environment variables sorted alphabetically

This is particularly useful for:
- Debugging workflow issues
- Understanding what data is available in your GitHub Actions environment
- Troubleshooting context-dependent logic