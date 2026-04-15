# BUG-01: Subrogation Not Triggered When Liability Assigned to Third Party

## Steps to Reproduce
1. Create a new claim with both insured and third-party exposures
2. Set insured liability to 0%
3. Assign third-party liability between 1%–100%
4. Save and process the claim
5. Issue a payment from the first-party exposure

## Expected Result
System should automatically trigger, and the claim should be flagged for recovery review.

## Actual Result
Subrogation workflow is not triggered, and no recovery activity is initiated.

## Severity
High

## Priority
High

## Impact
This issue may result in missed subrogation opportunities and potential financial loss.
