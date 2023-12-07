# JCL Script

## Overview

This is a JCL script for IBM's mainframe OS - z/OS. The script's primary purpose is to create a schedule for the Metro North train line from Poughkeepsie to New York City (NYC), focusing on peak hour operations.

## Script Functionality

The JCL script utilizes the `IEBGENER` utility program, which is a standard data copying tool in mainframe systems. The script is divided into several steps, each corresponding to a different station on the Metro North line. It compiles information about train stations and peak fare hours into a formatted schedule.

## Structure

The script is organized into multiple sections, each beginning with a unique step name and executing the `IEBGENER` program:

- **Header Section (`HEADER`):** Sets up the introductory message for the schedule.
- **Station Information Sections (`POK`, `NHB`, `BEACON`, etc.):** Each section adds details about a specific station, including its distance from NYC.
- **Peak Fare Information Section (`PEAKINFO`):** Provides information about peak and off-peak fare hours.

## File Descriptions

- **SYSUT1 DD Statements:** Used to input the specific data for each station or fare information.
- **SYSUT2 DD Statements:** Specifies the dataset names and attributes for storing the compiled schedule.
- **USER.JCL3OUT:** Is an example of the output.

## Usage

This script is intended to be run on an IBM mainframe system. Users can modify the station names and distances as per their requirements.

## Customization

You can customize the script by altering the data in the `SYSUT1` DD statements or by adding/removing steps for different stations.

## Note

This script serves as an example of using JCL and `IEBGENER` for creative data processing tasks. It demonstrates the versatility of mainframe utilities in handling various types of information, beyond traditional file copying and data management.
