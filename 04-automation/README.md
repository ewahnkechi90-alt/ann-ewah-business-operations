# Automation

## Objective

The automation was designed to reduce repetitive manual work and ensure that newly created onboarding tasks are initially assigned to the Operations Coordinator.

## Business Rule

Every new onboarding task should initially be reviewed by Ann, who oversees operations.

Ann then reviews the request and determines the appropriate staff member based on the nature of the work.

## Automation Logic

Trigger:
A new task is created.

Action:
The task is automatically assigned to Ann.

## Why This Was Automated

The initial assignment is predictable and consistent because every new onboarding task requires Ann's initial review.

Automating this step reduces the risk of newly created tasks being left unassigned.

## Human Decision Point

The automation does not automatically determine the final specialist.

Ann reviews the request and decides whether the task should be handled by:

- Michael — Client Support
- Sarah — Document Preparation
- David — Data Cleaning

This preserves human judgment where the appropriate assignment depends on the nature of the request.

## Testing

A test task named "Automation Test" was created to verify that the automation worked as expected.

The test confirmed that the newly created task was automatically assigned to Ann.

## Key Learning

Automation should be used for predictable, repeatable business rules while preserving human judgment where decisions require context.

Principle:

"Automate the predictable; preserve the judgment."

## Evidence

### Automation Rule

![ClickUp Automation Rule](clickup-automation-rule.png)

### Automation Test

![ClickUp Automation Test](clickup-automation-test.png)
