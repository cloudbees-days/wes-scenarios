# Wes Mimic Scenarios

Official scenario pack for CloudBees demo scenarios. Used with [Mimic](https://github.com/cb-demos/mimic).

## What is a Scenario Pack?

A scenario pack is a git repository containing YAML scenario definitions that Mimic can load and execute. Each scenario defines:
- GitHub repositories to create from templates
- CloudBees Platform components, environments, applications, and feature flags
- Parameter schemas for customization
- Computed variables and conditional file operations

## Using This Pack

This pack is automatically added when you run `mimic setup` for the first time.

To add it manually:

```bash
mimic scenario-pack add official https://github.com/cb-demos/mimic-scenarios
```

Then use the scenarios:

```bash
# List available scenarios
mimic list

# Run a scenario
mimic run hackers-app
```

## Available Scenarios

- **hackers-app**: Full Hackers App demonstration with three microservices
- **hackers-organized**: Organized variant of Hackers App with monorepo structure
- **java-gha**: Java application with GitHub Actions integration

## Creating Your Own Scenario Pack

Want to create custom scenarios for your team? Simply:

1. Create a new git repository (e.g., in `cb-demos` or your team's GitHub org)
2. Add YAML scenario files (see [scenario format documentation](https://github.com/cb-demos/mimic/blob/main/scenarios/README.md))
3. Add the pack to Mimic:

```bash
# Public repo
mimic scenario-pack add my-team https://github.com/cb-demos/my-team-scenarios

# Private repo (uses your SSH keys)
mimic scenario-pack add my-team git@github.com:myorg/my-scenarios.git
```

## Contributing

To add a new scenario to this official pack:

1. Add your scenario YAML file to this repository
2. Test it with Mimic locally
3. Submit a PR to this repo

For scenario format documentation, see [Mimic's scenario authoring guide](https://github.com/cb-demos/mimic/blob/main/scenarios/README.md).
