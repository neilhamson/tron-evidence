# MI1 Authority Boundary

## Purpose

MI1 is designed to participate in software-development work without receiving unrestricted authority over the project, repository or production environment.

This document describes the authority boundary demonstrated by the current MI1 development workflow.

## Human authority

Consequential changes require explicit human approval.

A proposed change is not equivalent to permission to apply it.

The demonstrated development sequence is:

`inspect → propose → human approval → apply → validate → controlled commit`

The human operator retains authority to reject or alter the proposed course of action.

## Repository boundary

MI1 can be configured with a repository capability profile defining what work is permitted.

A profile can constrain:

- editable directories
- editable file extensions
- diagnostic commands
- maximum number of changed files
- recursive editing
- approved project tooling

The public hamson.tech repository contains an example capability profile at:

`.mi1/repository.json`

## File-change boundary

MI1 changes are intended to remain within the explicitly permitted project scope.

For the demonstrated hamson.tech integration, editable source was restricted to selected application directories and supported source-file types.

The repository profile also limited the number of files that could be modified within a proposed change set.

## Validation boundary

An approved write does not by itself complete a development cycle.

Repository-defined validation must run after the approved modification.

For the demonstrated hamson.tech cycle, validation included:

- lint validation
- production-build validation

A validation failure prevents the workflow from being treated as a successfully completed controlled cycle.

## Version-control boundary

MI1 demonstrated controlled creation of a local Git commit after approval and successful validation.

The demonstrated workflow did not grant MI1 remote Git push authority.

Publication therefore remained a separate human-controlled action.

## Deployment boundary

MI1 was not granted production deployment authority during the demonstrated development cycle.

Creating a validated local commit and deploying software are intentionally separate operations.

## Model boundary

The reasoning model used by MI1 is a component of the development workflow rather than the authority holder.

Model output can contribute proposals and reasoning, but project authority is constrained by the surrounding MI1 control system and explicit human decisions.

## Current evidence

The first recorded complete external-repository development cycle is documented at:

`records/2026-09-20-controlled-development-cycle.md`

The demonstrated sequence was:

1. inspect
2. propose
3. explicit human approval
4. apply
5. validate
6. controlled local commit

Remote publication remained outside MI1 authority.

## Scope

This document describes the demonstrated MI1 control model.

It should not be interpreted as evidence that every possible MI1 configuration, task or future implementation uses identical restrictions.

Additional capabilities require their own evidence and authority definitions.
