# AxolotlBucketLabs Role Permissions

This document defines the responsibilities, application criteria, and permission boundaries for AxolotlBucketLabs roles.

The machine-readable role data is stored in [`roles.json`](roles.json). Current member assignments are stored in [`members.json`](members.json). Project responsibility and repository access are stored in [`projects.json`](projects.json) and explained in [`PROJECTS.md`](PROJECTS.md). Update the related files in the same pull request when a role or project policy changes.

## Permission model

Roles describe responsibility and trust. A role does not automatically grant every permission associated with its scope.

- Discord roles identify a person's community role. Discord server permissions are configured separately.
- GitHub organization membership and repository access are separate decisions.
- Repository access should follow the least privilege needed for the project.
- A role application is a request for review. It does not guarantee approval, membership, or repository access.
- A project-specific role does not grant organization administration.
- AI-assisted contributions are welcome when the contributor understands, reviews, tests, and takes responsibility for the submitted work.

## Role matrix

| Role | Scope | Assignment | Default GitHub access | Main responsibility |
| --- | --- | --- | --- | --- |
| `Lab Founder` | Organization | Founder only. | Organization owner. | Owns the organization and makes final decisions about its direction, settings, members, and projects. |
| `Lab Associate` | Organization | Invitation only. | Intended `Maintain` access to all organization repositories. This role does not automatically make the person an owner. | Helps manage the organization, projects, applications, and members. |
| `Lab Fellow` | Recognition | Honorary assignment by the Lab Founder or Lab Associate. | None. | Recognizes a person who has earned broad respect from the organization's leadership and project members. This role has no administrative or project responsibility. |
| `Lab Member` | Organization | Invitation or approved application. | Organization member. The current base repository permission is `No permission`. Explicit team or repository access is required. | Participates in the organization and contributes to its projects. |
| `Lab Maintainer` | Project | Approved application or invitation. | Project-specific access based on the repository need. `Maintain` or `Write` may be appropriate, while `Admin` requires a separate decision. | Maintains the development, quality, issues, pull requests, and releases of an assigned project. |
| `Lab Collaborator` | Project | Approved application or invitation. | Outside collaborator with access only to selected repositories. | Contributes regularly to a project without becoming an organization member by default. |
| `Lab Contributor` | Community | Manual recognition after a meaningful contribution. | No default GitHub access. Public contribution remains possible without this role. | Receives recognition for meaningful work that improves an organization project. |

## Role requirements

### Lab Founder

`Lab Founder` is reserved for the founder and owner of AxolotlBucketLabs. Applications are not accepted.

The founder controls organization ownership, billing, organization settings, member invitations, repository creation, repository visibility, and final role decisions.

### Lab Associate

`Lab Associate` is a trusted co-founder or administrator who helps manage the organization, its projects, and its members. It is assigned by the Lab Founder only. The intended repository policy gives this role `Maintain` access to all organization repositories without making the person a GitHub organization owner.

The role requires demonstrated trust, sound judgment, reliable communication, and a willingness to take responsibility for organization work. An associate should receive only the GitHub and Discord permissions needed for the delegated responsibilities.

### Lab Fellow

`Lab Fellow` is an honorary recognition role for a person who has earned broad respect from the Lab Founder, Lab Associates, Lab Members, and Lab Maintainers. It is assigned by the Lab Founder or Lab Associate and is not open to applications.

This role grants no Discord permission, private channel access, GitHub organization membership, repository access, project responsibility, or administrative authority. It exists only to recognize the person's standing in the community.

### Lab Member

`Lab Member` is an official member of the GitHub organization. Applications and invitations are accepted.

Applicants should demonstrate basic development experience, trustworthy collaboration, and a willingness to contribute. Extensive experience is not required. Developers who use AI tools or coding agents are welcome when they review, understand, test, and take responsibility for their work.

Membership does not automatically grant access to every repository. The current organization base permission is `No permission`, so access to a private or restricted repository must be granted separately.

### Lab Maintainer

`Lab Maintainer` is responsible for the ongoing development, maintenance, and quality of at least one organization project. This role is project-specific and does not automatically grant organization administration.

An applicant may propose an existing plugin or library for maintenance by AxolotlBucketLabs. The project must fit the organization, have suitable licensing, and have a realistic maintenance plan. A maintainer should be able to review contributions, make technical decisions, keep the project healthy, and communicate its compatibility and release status.

The GitHub permission is assigned per repository and recorded in [`projects.json`](projects.json). A maintainer does not receive `Admin` access by default.

### Lab Collaborator

`Lab Collaborator` is a trusted external collaborator with access to one or more selected organization repositories. This role does not make the person a member of the GitHub organization.

Applications may be considered after consistent, meaningful contributions. Three meaningful merged pull requests are a useful guideline, but contribution quality, communication, project fit, and trust matter more than a fixed number.

Repository access must match the work being done. An outside collaborator should not receive organization-wide access just because they collaborate on one project.

### Lab Contributor

`Lab Contributor` recognizes a community member who has made at least one meaningful contribution to an organization project.

Examples include fixing a real bug, adding a useful feature, improving performance, adding meaningful documentation, improving tests, or making another significant technical improvement. A trivial change made only to obtain the role does not qualify.

This role does not grant GitHub repository access, organization membership, merge permission, or project administration.

## Application and review

Apply through the [role application issue form](https://github.com/AxolotlBucketLabs/community/issues/new?template=role-application.yml). Include a public GitHub profile, relevant contributions or experience, and what you would like to help with.

Application issues are public. Do not include passwords, private contact details, personal documents, or other sensitive information. Use the [Discord server](https://discord.gg/Pk4FrNvHnM) when a private discussion is needed.

Applications are reviewed individually. Maintainers may request more information, approve a different role, or decline an application. Suggested contribution counts are guidelines and do not guarantee approval.

Roles may be combined when the responsibilities justify it. A role may be changed or removed when the responsibilities or trust behind it no longer apply.

## Current organization safeguards

The current GitHub organization settings establish these boundaries.

- Organization members have no base repository permission. Access must be granted through an authorized team or a repository-specific permission.
- Members cannot create private repositories in the organization.
- Members can currently create public repositories. This technical setting does not approve the project or grant its creator the `Lab Maintainer` role. New organization projects should still be proposed and reviewed.
- Private repository forking is disabled.
- Public Pages creation is disabled for members.
- Outside collaborators cannot request organization apps.
- Repository administrators cannot install GitHub Apps without organization approval.
- Only organization owners can change repository visibility, delete or transfer repositories, delete issues, or rename branches covered by organization rules.
- Members cannot create organization teams.

These platform settings can change independently from this document. A change to GitHub settings that affects role boundaries must be reflected here through a pull request.

## Principles

Roles recognize meaningful contributions, responsibility, and trust. They are not just titles.
