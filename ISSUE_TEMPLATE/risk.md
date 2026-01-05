name: Risk
description: Identify and manage a risk or opportunity affecting quality or delivery
title: "[Risk] "
assignees: []
body:

- type: markdown
  attributes:
  value: | ## Risk Identification
  Use this issue to record a risk or opportunity that could affect quality, delivery, or compliance.
  Risks may be mitigated, accepted, or closed when no longer applicable.

- type: textarea
  id: description
  attributes:
  label: Risk Description
  description: What could go wrong (or right)? Describe the risk clearly.
  placeholder: Describe the risk in plain language.
  validations:
  required: true

- type: checkboxes
  id: category
  attributes:
  label: Risk Category
  description: Select one or more categories.
  options: - label: Technical / design - label: Quality / conformity - label: Schedule / delivery - label: Supplier / manufacturing - label: Safety or compliance (design-related) - label: Knowledge / resource dependency - label: Other
  validations:
  required: true

- type: textarea
  id: affected
  attributes:
  label: Affected Area
  description: What products, systems, or activities could be affected?
  placeholder: | - Product / system: - Part / assembly / software component: - Project or release:
  validations:
  required: false

- type: textarea
  id: cause
  attributes:
  label: Cause / Trigger
  description: What underlying condition or event could trigger this risk?
  placeholder: Describe the root cause or trigger.
  validations:
  required: false

- type: dropdown
  id: impact
  attributes:
  label: Potential Impact
  description: What would be the impact if the risk materialised?
  options: - Minor - Moderate - Major - Critical
  validations:
  required: true

- type: dropdown
  id: likelihood
  attributes:
  label: Likelihood
  description: How likely is this risk to occur?
  options: - Low - Medium - High
  validations:
  required: true

- type: textarea
  id: mitigation
  attributes:
  label: Mitigation / Treatment Plan
  description: What actions are planned to reduce, manage, or accept this risk?
  placeholder: |
  Examples: - Design change - Additional verification - Supplier clarification - Schedule buffer - Explicit risk acceptance
  validations:
  required: false

- type: input
  id: owner
  attributes:
  label: Risk Owner
  description: Who is responsible for monitoring and managing this risk?
  placeholder: Name or role
  validations:
  required: true

- type: dropdown
  id: status
  attributes:
  label: Risk Status
  options: - Open - Mitigation in progress - Mitigated - Accepted - Closed
  validations:
  required: true

- type: textarea
  id: related
  attributes:
  label: Related Items
  description: Link related artefacts where applicable.
  placeholder: | - Requirement: - Feature / Task: - Verification: - Nonconformance: - Release:
  validations:
  required: false

- type: textarea
  id: review
  attributes:
  label: Review Notes
  description: Record review decisions or updates related to this risk.
  placeholder: |
  Examples: - Reviewed at design review - Accepted for development release - Escalated due to new information
  validations:
  required: false
