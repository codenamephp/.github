# Cookbook testing

This document describes the process for testing CodenamePHP Cookbooks

## Testing Prerequisites

A working Chef Workstation installation set as your system's default ruby and Vagrant or Docker for Test Kitchen

## Installing dependencies

Dependencies are installed automatically using Berkshelf.

## Testing

The following commands can be run in the project root:

- Rubocop is used for linitng and fixing style problems: `rubocop -a`
- Foodcritic is used for additional lints designed for chef: `foodcritic .`
- Unit Tests are run using rspec: `rspec`
- Integration tests are run using Test Kitchen:
  - For Dokken using Docker: `KITCHEN_LOCAL_YAML=kitchen.dokken.yml kitchen test`
  - For Vagrant: `kitchen test`
