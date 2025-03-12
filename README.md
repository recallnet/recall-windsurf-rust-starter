# Recall Windsurf Rust Starter

This repository serves as a starting point for developing Rust applications that interact with the Recall network using Windsurf IDE. It provides examples, tools, and guidance to help you get started quickly with Recall's Rust tooling ecosystem.

## 🔧 Recall Rust Tooling

Recall provides a comprehensive set of Rust libraries for interacting with the Recall network:

- **recall_sdk**: Core SDK containing functionalities for interacting with the Recall network, including working with buckets, managing credits, and handling network configurations.
- **recall_provider**: Library for interfacing with the Recall network via JSON-RPC.
- **recall_signer**: Library for managing wallets, signing transactions, and handling authentication.

All libraries can be found in the [rust-recall](https://github.com/recallnet/rust-recall) repository.

## 🚀 Getting Started with this Project in Windsurf

This project is designed to be used with Windsurf, an agentic IDE that helps you write better code faster. Follow these steps to make the most of this starter project:

### 1. Set Up Windsurf Global Rules

For an optimal Recall development experience, add the following global coding preferences in your Windsurf settings:

Windsurf -> Settings -> Global Rules

```
# Coding pattern preferences

– Always prefer simple solutions
– Avoid duplication of code whenever possible, which means checking for other areas of the codebase that might already have similar code and functionality
– Write code that takes into account the different environments: dev, test, and prod
– You are careful to only make changes that are requested or you are confident are well understood and related to the change being requested
– When fixing an issue or bug, do not introduce a new pattern or technology without first exhausting all options for the existing implementation. And if you finally do this, make sure to remove the old implementation afterwards so we don't have duplicate logic.
– Keep the codebase very clean and organized
– Avoid writing scripts in files if possible, especially if the script is likely only to be run once
– Avoid having files over 200–300 lines of code. Refactor at that point.
– Mocking data is only needed for tests, never mock data for dev or prod
– Never add stubbing or fake data patterns to code that affects the dev or prod environments
```

### 2. Review Local Rules

This repository already contains a `.windsurfrules` file with specific rules and examples for Recall Rust projects. This file includes:
- Documentation links
- Code examples for common Recall operations
- Instructions for adding dependencies to your Cargo.toml

Take time to review the `.windsurfrules` file to understand the project-specific guidelines and examples.

### 3. Create a Project Specification

To start building with Recall, prompt Windsurf Cascade to write a project specification in `command.md`:

1. In Windsurf, open a new chat with Cascade
2. Ask Cascade to create a project specification with a prompt like:

```
Can you write a project specification in command.md for a command line tool that polls and mirrors a remote Recall bucket hosted on testnet locally every 10 minutes? The tool should:
- Allow users to specify a source bucket address
- Create a local directory structure matching the bucket contents
- Sync new files and detect & update changed files
- Provide a simple configuration file for customizing behavior
- Show sync progress and status information
```

Your specification should thoroughly explain the project requirements, expected behavior, and any technical constraints.

### 4. Generate a Development Plan

Once you have a project specification:

1. Review the `command.md` file to ensure it captures your requirements
2. Ask Cascade to create a development plan:

```
Based on the command.md specification, can you create a development_plan.md file with a structured approach to implementing this project?
```

The development plan will break down the implementation into logical steps, creating a roadmap for your project.

### 5. Start Development

When you're satisfied with both the specification and development plan:

1. Ask Cascade to begin implementation:

```
I'm happy with the specification and development plan. Let's start implementing the project according to the development_plan.md.
```

Cascade will guide you through the implementation process, helping you write code that follows best practices for Recall development.

## 📚 Resources

- [Recall Network Documentation](https://docs.recall.network)
- [Rust Recall SDK GitHub Repository](https://github.com/recallnet/rust-recall)
- [Rust SDK Examples](https://github.com/recallnet/rust-recall/tree/main/sdk/examples)

## 🔄 Token and Credit Management

This starter project includes functionality to help users view their token balances (both Recall tokens and credits) and guide them through converting tokens to credits after the faucet funding step:

1. Check balances after faucet funding
2. If credits are 0, guide users to convert half of their tokens to credits
3. Skip conversion if credits are already available

This streamlined approach ensures users can quickly get started with the necessary resources for their Recall applications.

## 🤝 Contributing

We welcome contributions to improve this starter project! Please feel free to submit issues or pull requests to enhance the examples and documentation.
