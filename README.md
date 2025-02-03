# Inconsistent Style Application with @apply in Conditional Custom Directives

This repository demonstrates a bug encountered when using Tailwind CSS's `@apply` directive within conditional statements inside custom Vue directives.  The `@apply` directive sometimes fails to apply styles correctly when the condition changes.

## Bug Description

The core issue lies in the unpredictable behavior of `@apply` when embedded within a directive's conditional logic.  Styles might not be applied, or might be applied inconsistently, leading to visual discrepancies in the user interface.

## Reproduction Steps

1. Clone this repository.
2. Run `npm install` to install the dependencies.
3. Run `npm run serve` to start the development server.
4. Observe the button; the styles applied via `@apply` do not correctly reflect the conditional logic.

## Solution

The solution involves avoiding the use of `@apply` within conditional statements in custom directives.  Instead, leverage the more robust class binding system provided by Vue.js (`:class`) to manage styles dynamically based on conditions.