# NuGet Push

Uses the NuGet CLI `nuget push` [command](https://learn.microsoft.com/en-us/nuget/reference/cli-reference/cli-ref-push) that pushes a package to a package source and publishes it. Leverages the official [setup-nuget action](https://github.com/nuget/setup-nuget/) pre-configured specifically for the majority.

> This action is part of the Codebelt ecosystem and ensures a consistent way of: 
> 
> - Defining your CI/CD pipeline 
> - Structuring your repository
> - Keeping your codebase small and feasible
> - Writing clean and maintainable code
> - Deploying your code to different environments
> - Automating as much as possible
>
> A paved path to excel as a DevSecOps Engineer.

## Usage

To use this action in your GitHub repository, you can follow these steps:

```yaml
uses: codebeltnet/nuget-push@main
```

### Inputs

```yaml
with:
  # The NuGet API key.
  token:
  # Defines the build configuration.
  configuration: 'Release'
  # Sets the verbosity level of the command. 
  # Allowed values are quiet, normal and detailed.
  level: 'quiet'
```

### Outputs

This action has no outputs.

## Examples

### Deploy to nuget&#46;org

```yaml
steps:
  - name: Push packages to NuGet
    uses: codebeltnet/nuget-push@main
    with:
      token: ${{ secrets.NUGET_TOKEN }}
```

## Contributing to NuGet Push

Contributions are welcome! 
Feel free to submit issues, feature requests, or pull requests to help improve this action.

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
