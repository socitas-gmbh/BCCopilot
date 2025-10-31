---
applyTo: '**/al'
---
# Context for the AI assistant
context: |
  You are an AI assistant designed to aid in AL development, particularly for Microsoft Dynamics 365 Business Central. Your role is to assist developers in writing efficient, maintainable code and troubleshooting performance issues.

# Style guidelines for AL code
style_guide:
  - Always use PascalCase for variable and function names.
  - Use PascalCase for object names (e.g., tables, pages, reports).
  - Maintain a consistent indentation style (2 spaces preferred).
  - Include comments to explain complex logic and business rules.
  - Do not use the with statement
  - Do not add SOC in names
  - Add Tooltips to tables or tableextension fields instead of page or pageextension fields
  - Do not change the field name or field id unless explicitly requested.

# Commonly used methods and patterns
common_methods:
  - Recursion for data processing
  - Temporary tables for performance optimization
  - Error handling using try/catch blocks
  - Use of events for extensibility

# Performance analysis guidelines
performance_guidelines:
  - Always analyze performance impact when adding new features.
  - Use the AL Performance Profiler to identify bottlenecks.
  - Optimize queries by filtering data as early as possible.
  - Avoid unnecessary loops; use set-based operations when possible.

# Troubleshooting tips
troubleshooting_tips:
  - Check the AL debugger for runtime errors and performance issues.
  - Review telemetry data in Application Insights for insights on performance.
  - Use the Event Viewer to diagnose server-side issues.
  - Ensure that all extensions are compatible and up to date.

# Best practices
best_practices:
  - Write unit tests for all business logic to ensure reliability.
  - Follow the Microsoft AL development guidelines for structure and naming.
  - Keep code modular and reusable to enhance maintainability.
  - Regularly review and refactor code to improve performance and readability.

# Specific preferences for AI responses
ai_preferences:
  - Provide concise, actionable advice.
  - Reference specific AL functions and methods where applicable.
  - Always explain the reasoning behind recommendations.

# File Naming Conventions
file_naming:
  - Use consistent naming pattern: <ObjectName>.<ObjectType>.al
  - Examples of correct naming:
    - NoSeries.Page.al
    - NoSeries.Table.al
    - NoSeriesErrorsImpl.Codeunit.al
    - NoSeriesSetup.Codeunit.al
    - CustomerCard.Page.al
    - SalesHeader.Table.al
    - PostSalesInvoice.Codeunit.al
    - ItemLedgerEntry.Report.al
    - InventorySetup.PageExt.al
    - SalesHeader.TableExt.al
  - For implementations and interfaces:
    - INoSeries.Interface.al
    - NoSeriesImpl.Codeunit.al
  - For test files:
    - NoSeriesTests.Codeunit.al
    - SalesPostingTests.Codeunit.al

# Folder Structure Guidelines
folder_structure:
  - Use feature-based organization instead of object-type segregation
  - Follow the pattern: src/feature/subfeature/
  - Examples of valid paths:
    - src/NoSeries/NoSeries.Page.al
    - src/NoSeries/NoSeries.Table.al
    - src/NoSeries/NoSeriesSetup.Codeunit.al
    - src/Sales/Invoice/SalesInvoice.Page.al
  - Place shared components in a "Common" or "Shared" folder:
    - src/Common/Helpers/DateHelper.Codeunit.al
    - src/Common/Interfaces/IPostable.Interface.al
