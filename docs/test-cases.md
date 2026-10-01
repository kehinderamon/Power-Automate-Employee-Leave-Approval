# Test Cases

This document records the functional tests performed on the Employee Leave Approval Power Automate workflow.

| ID | Test Scenario | Input | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|
| TC01 | Standard leave request | 5 leave days | Standard approval route | Standard Leave route executed | Passed |
| TC02 | Extended leave request | 8 leave days | Manager + HR / extended route | Extended Leave route executed | Passed |
| TC03 | Invalid date range | End Date earlier than Start Date | Request rejected and flow terminated | Invalid request terminated | Passed |
| TC04 | Non-annual leave | Leave Type = Sick Leave | Other Leave route | Other Leave route executed | Passed |
| TC05 | Single-day leave | Start Date = End Date | Leave Days = 1 | Flow completed successfully with 1 leave day | Passed |

## Validation Summary

The workflow successfully handled:

- Valid leave requests
- Invalid date ranges
- Inclusive leave-day calculation
- Standard and extended leave durations
- Annual and non-annual leave types
- Single-day leave requests

## Notes

External SharePoint and email integration tests were not completed because the development environment restricted the required cross-tenant connector authentication.

The core Power Automate business logic was tested independently of these external integrations.
