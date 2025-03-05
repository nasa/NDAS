# NDAS Peer Review Tool

## Overview
The **NDAS Peer Review Tool** enhances collaboration and code quality by streamlining the peer review process. It automatically compares all modified files against their baselined version, allowing reviewers to focus on significant changes while running static and predefined VI Analyzer tests to ensure code integrity.

## Features
* **LabVIEW File Comparison**: Uses `LVCompare` to detect changes in LabVIEW files.
* **Text File Comparison**: Integrates with `TortoiseGitMerge` for reviewing text-based modifications.
* **Pause & Resume Reviews**: Allows reviewer to pause and resume the review at any time.
* **Iterative Review Support**: Compares the current version against the last reviewed version for multi-stage reviews.
* **Bulk Review Capability**: Allows files with similar changes to be reviewed simulatenously.
* **Integrated Right-Click Options** - Allows access to assist in peer review reporting.
* **Automated Analysis**: Runs a predefined set of `VI Analyzer` tests to identify potential issues.
* **Static Analysis**
    - **Reentrancy Check** - Ensures changes in reentrancy are intentional.
    - **Readability** - Ensures front panels and block diagrams fit within the primary monitor's **1920 x 1080** resolution bounds.
    - **Cyclomatic Complexity** - Encourages lower complexity to improve modularity.
    - **Node Count** - Promotes a lower node count for better readability and maintainability.
    - **LabVIEW Version** - Displays the LabVIEW version of each file to minimize versioning conflicts and ensure compatibility.
    - **Lines Added & Removed** - Helps reviewers gauge the size and complexity of modifications in text-based files.


## Installation

## Prerequisites

* LabVIEW 2020 or later
* Windows 10 or later
* Git (for version control integration)
* TortoiseGit (TortoiseGitMerge is used for comparing differences in text-based files)

## Steps

* Clone the repository:

        git clone https://github.com/nasa/NDAS.git
* Open `Peer Review Tool.vi` in LabVIEW.
* On first run, the `Peer Review Tool.vi` will create a configuration file in the default LabVIEW data directory (i.e. C:\Users\xxx\Documents\LabVIEW Data\NDAS Peer Review Tool.ini).
* Edit configuration options in `NDAS Peer Review Tool.ini`.

* Rerun `Peer Review Tool.vi`.
* Click **Review Branch** to initiate a peer review.

## Contributing

We welcome any contributions! Follow these steps:
* Clone the repository.
* Create a feature branch.
* Commit your changes with descriptive messages.
* Submit a pull request for review.
