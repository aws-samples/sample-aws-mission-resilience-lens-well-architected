# AWS Mission Resilience Lens

## Description
The AWS Mission Resilience Lens (MRL) is a targeted evaluation framework for defense and national security workloads. This lens includes best practices based on our experience reviewing these architectures, and includes additional content from both the AWS Operational Readiness Review program and the AWS Well-Architected Framework's Reliability pillar. AWS recommends supplementing this work with a full Well-Architected review when time permits. Reviews should be conducted at least annually or after significant architectural changes.

Created as a custom lens for the WAFR tool:
[WAFR Custom Lenses](https://docs.aws.amazon.com/wellarchitected/latest/userguide/lenses-custom.html)


## Installation

The AWS Mission Resilience Custom Lens (MRL) is a JSON file that can be obtained from AWS Samples or your AWS Account Team. To use the MRL:

1. Access the AWS Well-Architected Tool console and navigate to the "Custom lenses" section.
2. Select "Create custom lens" or "Import lens" to upload the MRL JSON file.
3. Review the imported lens content and make any necessary adjustments.
4. Publish the lens to make it available for use in workload reviews.
5. Navigate to the desired workload, select "View details," and choose the MRL from the "Custom lenses" option.
6. Use the MRL to conduct architecture reviews that incorporate architecture questions and best practices tailored around mission resilience.

For more information on AWS Well-Architected Lenses, refer to the [AWS Well-Architected documentation](https://docs.aws.amazon.com/wellarchitected/latest/userguide/lenses.html).

## Prerequisites
We recommend preparing the following items before the review:
* A system diagram showing the infrastructure and data/network flows, including any relevant security boundaries.
* Note any Cross-domain Systems that the workload depends on.
* Note any Service Level Agreements or Service Level Objectives for the workload.
* Provide a list of AWS account numbers that make up the system.
* Provide a list of AWS regions used in the architecture.
* Provide a list of AWS services used in the architecture.
* Provide a list of Classification levels that the workload transcends.
* Provide a list of customer-facing APIs or other interfaces provided by your workload.
* Provide a list of external resources (or systems) that the workload depends on.
* Operational category of the workload (for example: Mission Critical (MAC-I), Mission Essential (MAC-II), Mission Support (MAC-III)).

## Contributing
Please submit issues for any errors/corrections/contributions

## Answering Questions

Questions in this lens follow different selection patterns. Understanding these patterns helps ensure accurate responses during a review.

### Multi-select best practices
Most questions present a list of best practices where you should check all that apply. For example, "How do you back up data?" lists several backup practices — select every one your workload follows.

### Mutually exclusive choices
Some questions describe different states of the same thing, where only one option applies. For example, "Is each component of your workload deployed to multiple locations?" presents deployment patterns (multi-region, multi-AZ, single AZ) — select the one that best describes your current architecture.

### Grouped choices
Some questions contain logical groups where you would typically pick one from each group. For example, "What level of AWS Support do you have?" asks about both your AWS support tier (Enterprise, Business, or Developer) and your non-AWS dependency coverage (full, partial, or none). Select one from each group that matches your current state.

### Anti-pattern and state-based choices
Some questions include choices that describe anti-patterns or less-than-ideal states alongside best practices. These are included to capture your workload's current state accurately, not as goals to achieve. For example, "Developer Support" or "Single AZ only" are options you would select if they describe your current situation. The improvement plan report uses tags to help distinguish these from best practices (see Understanding Improvement Plans below).

## Understanding Improvement Plans

When you complete a review using this lens, the report generates improvement plans for any choices that were not selected. Each improvement plan includes guidance relevant to that specific choice. To help readers quickly understand the context of each improvement plan, we use three tags:

### [Anti-pattern]
These flag practices that should be actively avoided. If you see an anti-pattern improvement plan on your report and you are not doing the thing it describes, no action is needed — the plan is confirming that you are already avoiding a risky practice. Example:

> [Anti-pattern: Single AZ only] Single-AZ deployments present significant availability risks with no resilience against zone failures. Deploy across at least two Availability Zones to establish baseline resilience.

### [Partial implementation]
These indicate practices that represent an incomplete or intermediate maturity level. They are not necessarily bad, but they fall short of the best practice. If you see one on your report, it may describe a stage you have already moved past. Example:

> [Partial implementation: Defined roles, partial] Defined reliability roles require complete implementation and clear accountability measures to be fully effective. Progress toward a comprehensive program to ensure consistent management of resilience risks.

### [Awareness gap]
These highlight areas where visibility or understanding is lacking. They typically relate to choices where a review, evaluation, or assessment has not been performed. Example:

> [Awareness gap: SLAs not reviewed] Unreviewed dependency SLAs represent unknown risks to mission readiness. Conduct a comprehensive review of all dependency SLAs and assess their impact on overall workload availability.

### Improvement plans without tags
Choices that represent best practices do not carry a tag. When these appear on your report as unchecked, the improvement plan provides direct guidance on how to adopt that best practice.

This library is licensed under the MIT-0 License. See the LICENSE file.