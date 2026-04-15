# Test Cases

## TC-01: Submit New Claim

**Priority:** P1

**Preconditions:**
- User is on the claims submission page
- Valid policy exists

**Steps:**
1. Navigate to claims submission page
2. Enter valid policy number
3. Upload required documents
4. Submit claim

**Expected Result:**
Claim is successfully created and a unique claim number is generated.

---

## TC-02: Missing Documentation

**Priority:** P1

**Preconditions:**
- User is on the claims submission page
- Valid policy exists

**Steps:**
1. Navigate to claims submission page
2. Enter valid claim information
3. Do NOT upload required documents
4. Submit claim

**Expected Result:**
System displays an error message indicating required documents are missing and prevents claim submission.

---

## TC-03: Duplicate Claim Detection

**Priority:** P2

**Preconditions:**
- An existing claim with the same details has already been submitted

**Steps:**
1. Navigate to claims submission page
2. Enter the same claim details used in an existing claim
3. Upload required documents
4. Submit claim

**Expected Result:**
System detects and flags the duplicate claim, preventing submission or notifying the user of an existing related claim.

---

## TC-04: Subrogation Triggered

**Priority:** P1

**Preconditions:**
- Claim contains both insured and third-party exposures
- First-party payment can be issued

**Steps:**
1. Set insured liability to 0%
2. Assign third-party liability between 1%–100%
2. Save and process the claim
4. Issue a payment from the first-party exposure

**Expected Result:**
System automatically triggers the subrogation workflow and flags the claim for recovery review.

---

## TC-05: Invalid Policy Number

**Priority:** P1

**Preconditions:**
- User is on the claims submission page

**Steps:**
1. Navigate to claims submission page
2. Enter an invalid policy number format
3. Complete all other required fields
4. Submit claim

**Expected Result:**
System displays an error indicating the policy number is invalid and prevents claim submission.
