# Contributing to Bastyon

The Bastyon project operates an open contributor model where anyone is welcome to contribute towards development in the form of peer review, testing, and patches. This document explains the practical process and guidelines for contributing.

First, in terms of structure, there is no particular concept of "Bastyon developers" in the sense of privileged people. Open source often naturally revolves around a meritocracy where contributors earn trust from the developer community over time. Nevertheless, some hierarchy is necessary for practical purposes. As such, there are repository maintainers who are responsible for merging pull requests, the release cycle, and moderation.

## Getting Started

New contributors are very welcome and needed.

Reviewing and testing is highly valued and the most effective way you can contribute as a new contributor. It also will teach you much more about the code and process than opening pull requests. Please refer to the [peer review](#peer-review) section below.

Before you start contributing, familiarize yourself with the Bastyon build system and tests:
- Browser-based application architecture
- Proxy server SSL handling
- Blockchain node operation
- Content validation and consensus mechanisms

## Contributor Workflow

The codebase is maintained using the "contributor workflow" where everyone without exception contributes patch proposals using "pull requests" (PRs). This facilitates social contribution, easy testing, and peer review.

To contribute a patch, the workflow is as follows:

1. Fork repository
2. Create topic branch
3. Commit patches

### Component Repositories

For different types of contributions, use the appropriate repository:
- Frontend changes: browser-based Bastyon app repository
- Proxy server changes: SSL proxy repository
- Node changes: blockchain node repository
- Core protocol changes: main protocol repository

### Committing Patches

In general, commits should be atomic and diffs should be easy to read. For this reason, do not mix any formatting fixes or code moves with actual code changes.

Commit messages should be verbose by default consisting of:
- Short subject line (50 chars max)
- Blank line
- Detailed explanatory text

Example:
```
consensus: Update content validation rules for multimedia

This commit implements new validation rules for multimedia content
in the blockchain nodes. The changes include:
- Enhanced format verification
- Size limit enforcement
- Metadata validation
```

### Creating the Pull Request

The title of the pull request should be prefixed by the component or area that the pull request affects. Valid areas are:

- `consensus` for changes to consensus critical code
- `proxy` for changes to the SSL proxy
- `frontend` for changes to the browser app
- `node` for changes to blockchain nodes
- `protocol` for changes to the network protocol
- `doc` for changes to documentation
- `test` for changes to test suite
- `build` for build system changes

### Content Flow Considerations

When making changes, consider the content flow architecture:
1. Browser-based content creation
2. HTTPS transmission to proxy
3. Proxy processing
4. Node validation
5. Network consensus
6. Confirmation flow

## Peer Review

Anyone may participate in peer review which is expressed by comments in the pull request. Project maintainers take into account the peer review when determining if there is consensus to merge a pull request.

### Review Types

#### Conceptual Review
- `Concept ACK` - Agrees with the general goal
- `Concept NACK` - Disagrees with the general goal (must provide reasoning)
- `Approach ACK/NACK` - Agrees/disagrees with implementation approach

#### Code Review
After conceptual agreement, reviewers should:
1. Test the code (manual + automated tests)
2. Review the code quality
3. Verify consensus compliance
4. Check documentation

### Finding Reviewers

- Look for previous contributors in the area you're changing
- Ask in development channels
- Be patient and respect maintainers' time
- Contribute reviews to others while waiting

## Technical Requirements

### Code Quality
- Follow existing code style
- Write clear documentation
- Include comprehensive tests
- Handle errors appropriately
- Consider performance implications

### Testing Requirements
1. Unit tests for new functionality
2. Integration tests for system interactions
3. Consensus validation tests
4. Network propagation tests
5. Performance benchmarks

### Security Considerations
- Follow security best practices
- Validate all inputs
- Protect user privacy
- Consider network attack vectors
- Implement proper encryption

## Decision Making Process

Whether a pull request is merged into Bastyon rests with the project maintainers. Pull requests must:

1. Have a clear use case
2. Be well peer-reviewed
3. Include appropriate tests
4. Follow code style guidelines
5. Not break existing tests
6. Include relevant documentation

Changes affecting consensus rules require:
- Extensive discussion
- Formal proposal
- Network-wide consideration
- Careful security review

## Credits
This contribution guidelines have been largerly based on the [Bitcoin's Contributing document](https://github.com/bitcoin/bitcoin/blob/master/CONTRIBUTING.md)

## Copyright

By contributing to this repository, you agree to license your work under the project's license unless specified otherwise. Any work contributed where you are not the original author must contain its license header with the original author(s) and source.
