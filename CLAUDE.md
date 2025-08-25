# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## GitBook Documentation

The official GitBook documentation is available at: https://gitbook.com/docs

## Repository Overview

This is a GitBook documentation repository for AeroQuote.com - an air charter quote software platform. The documentation is organized in Markdown files with GitBook-specific formatting and is split into guides for two main audiences: Charter Operators (who operate fleets directly) and Brokers (who organize charter flights via Charter Operators).

## Repository Structure

The documentation follows a hierarchical structure:
- `README.md` - Main welcome page with GitBook front matter
- `SUMMARY.md` - Table of contents defining the documentation structure
- `getting-started/` - Initial setup and concept explanations
- `guides/` - Main documentation organized by feature areas
- `overview/` - High-level product information

## GitBook-Specific Conventions

This repository uses GitBook formatting:
- YAML front matter for page metadata (description field)
- GitBook-specific tags like `{% content-ref %}`, `{% hint %}`, `{% endcontent-ref %}`
- Image references to `.gitbook/assets/` directory
- Markdown with HTML attributes for styling (e.g., `<a href="#" id="">`)

## Key Concepts

The documentation covers the AeroQuote job flow:
1. **Requests** - Initial customer charter requests with automated pricing estimates
2. **Quotes** - Central system feature with Options for different aircraft/services
3. **Bookings** (Operators only) - Converted accepted quotes with crew/passenger management

## Documentation Guidelines

When editing documentation:
- Preserve GitBook-specific formatting and tags
- Maintain consistent structure with existing guides
- Clearly indicate audience with "(Operators)" or "(Brokers)" in titles when content is role-specific
- Use descriptive front matter for page descriptions
- Follow the existing heading hierarchy and markdown conventions

## Related Repository

The main AeroQuote application repository is located at `/Users/tompwhite/Sites/aeroquote`. This is a Laravel application using:
- **Event Sourcing** with Spatie Event Sourcing for Quote and Booking entities
- **Livewire** for interactive UI components
- **Filament** for admin panels
- **Multi-tenancy** with operator-based data isolation
- **External integrations** with QuickBooks, Xero, Firestore, and iFlightPlanner

When updating documentation, ensure it accurately reflects the application's actual implementation and features found in the main codebase.