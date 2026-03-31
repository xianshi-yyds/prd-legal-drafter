# Document Scope Gate

Use this gate before drafting to decide what kind of document can honestly be produced from the available facts.

## Step 1: Identify the Product Form

Classify the target product into one of these buckets:

- direct online service or web app
- online service plus connected hardware
- hardware product with optional ecosystem features
- enterprise platform
- SDK, API, or technical support layer

## Step 2: Check Whether a Full Privacy Policy Is Actually Supported

A full standalone privacy policy is appropriate only when the materials clearly support most of the following:

- operator or controller identity
- account or access path
- concrete personal information categories actually collected
- purposes of processing
- third-party processors or service providers if mentioned
- storage, deletion, or rights-handling path at least at a basic level

If most of the above are missing, do not draft a polished, full-fact privacy policy as if the facts were settled.

## Step 3: Hardware Product Rule

If the PRD is mainly a hardware or industrial design document:

- do not assume a full online privacy stack exists
- do not automatically pull in ecosystem services, apps, cloud services, or account systems unless the PRD expressly ties them to the product
- do not treat companion-service names as confirmed scope merely because they are plausible for the brand
- prefer a narrower output such as:
  - a conservative privacy draft with many placeholders, or
  - a recommendation that privacy facts are insufficient for a clean final draft

## Step 4: Service Boundary Rule

Separate these concepts:

- device-local processing
- account-system processing
- companion-app processing
- cloud-service processing
- third-party service processing

Do not merge them into one privacy narrative unless the source materials clearly do so.

## Step 5: Unsupported Fact Red Flags

If any of the following appear in a draft without clear support, stop and replace with placeholders or remove:

- operator entity name
- specific ecosystem account names
- exact collection categories
- named analytics, cloud, support, or delivery vendors
- security controls such as encryption-at-rest, audits, or employee training
- legal bases such as consent, contract necessity, or legitimate interests
- storage location and cross-border transfer claims

## Step 6: Output Decision

Choose one of these output modes:

- `full draft`: enough facts exist for a reasonably complete external draft
- `conservative draft`: structure is complete but many factual clauses remain placeholders
- `insufficient facts`: explain that a clean privacy policy or agreement cannot honestly be finalized yet

Prefer `conservative draft` over fabricated completeness.
