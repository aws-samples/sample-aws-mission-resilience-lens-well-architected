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

## Creating an MRL Spreadsheet for offline use:
The create-spreadsheet folder contains a python script that will export the content from .json to .xlsx.
1.  From /create-spreadsheet folder: pip install -r requirements.txt
2.  python3 create-mrl-spreadsheet.py
3.  Enter the path to the .json file, for example: ../mrl-05.json
4.  The script will return: Done! Processed '../mrl-v0.5.json' and saved to: MRL_Assessment.xlsx

## Contributing
Please submit issues for any errors/corrections/contributions

## License
This library is licensed under the MIT-0 License. See the LICENSE file.
