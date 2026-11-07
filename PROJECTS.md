# Project Ownership and Access

This document explains how AxolotlBucketLabs records project responsibility and repository access. The machine-readable registry is available in [`projects.json`](projects.json).

## How the registry works

`projects.json` records the declared organization policy for each repository. It identifies the project type, current status, assigned members, role IDs, and intended GitHub repository permission.

The registry is a policy document. It does not prove that GitHub has already applied every permission. After an assignment changes, an organization owner must verify the live GitHub repository access separately.

Every member reference must match a GitHub username in [`members.json`](members.json), and every role reference must match an ID in [`roles.json`](roles.json).

## Organization access policy

| Role | Project scope | Intended repository permission |
| --- | --- | --- |
| `Lab Founder` | All projects | `Admin` |
| `Lab Associate` | All projects | `Maintain` |
| `Lab Member` | No default project access | `None` |
| `Lab Maintainer` | Assigned projects | `Maintain` |
| `Lab Collaborator` | Selected projects | `Write` by default, adjusted to the project need |
| `Lab Contributor` | No default project access | `None` |
| `Lab Fellow` | No project access | `None` |

`Lab Associate` access is intended for trusted organization administrators who need to maintain all repositories. It does not make the person a GitHub organization owner.

`Lab Member` is the normal organization membership role. A member can receive access to a specific repository later without receiving access to every project.

`Lab Maintainer` describes project responsibility. The role is granted through an assignment to one or more specific projects.

`Lab Fellow` and `Lab Contributor` are recognition roles. Neither role grants GitHub repository access.

## Repository permission levels

| Permission | Meaning |
| --- | --- |
| `Admin` | Full repository administration, including settings and access management |
| `Maintain` | Project maintenance, code review, pull requests, releases, and workflows without full repository administration |
| `Write` | Push code and contribute actively to the repository |
| `Triage` | Manage issues and pull requests without pushing code |
| `Read` | View and discuss the repository |
| `None` | No repository access is assigned by the organization policy |

The permission names follow GitHub repository roles. A repository administrator must review sensitive permissions, including Actions secrets, workflow access, protected branches, and repository settings, before assigning a role.

## Current project registry

The organization currently has 13 active repositories in the registry.

| Project | Type | Declared managers |
| --- | --- | --- |
| [`.github`](https://github.com/AxolotlBucketLabs/.github) | Organization configuration | NhanAZ with `Admin`, jeantkg with `Maintain` |
| [`arithmexp`](https://github.com/AxolotlBucketLabs/arithmexp) | Virion | NhanAZ with `Admin`, jeantkg with `Maintain` |
| [`await-generator`](https://github.com/AxolotlBucketLabs/await-generator) | Library | NhanAZ with `Admin`, jeantkg with `Maintain` |
| [`axolotl-pm-skill`](https://github.com/AxolotlBucketLabs/axolotl-pm-skill) | Skill | NhanAZ with `Admin`, jeantkg with `Maintain` |
| [`community`](https://github.com/AxolotlBucketLabs/community) | Community | NhanAZ with `Admin`, jeantkg with `Maintain` |
| [`DevTools`](https://github.com/AxolotlBucketLabs/DevTools) | Tool | NhanAZ with `Admin`, jeantkg with `Maintain` |
| [`FormAPI`](https://github.com/AxolotlBucketLabs/FormAPI) | Library | NhanAZ with `Admin`, jeantkg with `Maintain` |
| [`PersonaSkin`](https://github.com/AxolotlBucketLabs/PersonaSkin) | Plugin | NhanAZ with `Admin`, jeantkg with `Maintain` |
| [`pmforms`](https://github.com/AxolotlBucketLabs/pmforms) | Library | NhanAZ with `Admin`, jeantkg with `Maintain` |
| [`PureChat`](https://github.com/AxolotlBucketLabs/PureChat) | Plugin | NhanAZ with `Admin`, jeantkg with `Maintain` |
| [`PurePerms`](https://github.com/AxolotlBucketLabs/PurePerms) | Plugin | NhanAZ with `Admin`, jeantkg with `Maintain` |
| [`ScoreHud`](https://github.com/AxolotlBucketLabs/ScoreHud) | Plugin | NhanAZ with `Admin`, jeantkg with `Maintain` |
| [`SimplePacketHandler`](https://github.com/AxolotlBucketLabs/SimplePacketHandler) | Virion | NhanAZ with `Admin`, jeantkg with `Maintain` |

## Updating project assignments

When adding a repository, add one entry to `projects.json` with a stable ID, repository URL, type, status, and assignments.

When changing a manager or repository permission, update the JSON registry and verify the corresponding GitHub settings in the same change.

Do not add a person to a project only because they are a Discord member. The assignment should match their GitHub role, responsibility, and actual need for access.
