# Windows Forensic Investigation Report

Case Name: Windows Investigation Hunt - Laptop1Final.E01
Report Date: 02/16/2026
Prepared By: Arash Mahboobhosseini and Vivian John Goshashy
Group: Group 6
Course: SEC 350HB – Digital Forensics
Instructor: Evan Drake


## Executive Summary

This report details the forensic examination of a Windows 10 Home system (image file: Laptop1Final.E01). The investigation focused on identifying key system information, user activity, connected devices, and recovered artifacts. The forensic image was verified using MD5 hashing (a5a52c89ebd24b725a1bcd6462bf7670), confirming evidence integrity throughout the examination process.

Key findings include:

* System hostname: DESKTOP-SKPTDIO

* Windows 10 Home (Build 22000) with evidence of a previous installation

* Connected Apple iPhone (5 series) device

* User Patrick with Microsoft account (pbentley0107@gmail.com)

* Recovered deleted Minecraft installer from Recycle Bin

* Evidence of user playing "Never Gonna Give You Up" 9 times

* Multiple installed applications including gaming and development tools


## Table of Contents

1. Evidence Integrity Verification
   
2. System Identification

3. Operating System Analysis

4. Time Zone Configuration

5. Connected Devices Analysis

6. User Web Activity

7. Recycle Bin Recovery

8. Master File Table ($MFT) Analysis

9. User Account Analysis (SAM Registry)

10. Installed Programs

11. Interesting Findings (Fun Facts)

12. Methodology

13. Conclusion


### 1. Evidence Integrity Verification
| Field    | Value     |
| --- | --- |
|  Image File   |  Laptop1Final.E01    |
|  MD5 Hash   |   a5a52c89ebd24b725a1bcd6462bf7670   |
|  SHA1   |  Not calculated    |
|   SHA-256  |   Not calculated   |
|  Image Size   |      |
|  Sector Size   |      |
|  Time Zone   |  America/Los Angeles    |
|  Drive Model   |     |
|   Serial Number  |     |
|  Acquisition Date   |       |
| Acquisition Tool |     |


### ✅ Verification Confirmed: The MD5 hash stored in the E01 metadata matches the computed hash, confirming the image is an exact, unaltered copy of the original evidence. SHA1 and SHA-256 were not calculated during acquisition, which is why Autopsy displays "Not calculated" – this does not affect evidence validity.


### 2. System Hostname

The hostname was extracted from the SYSTEM registry hive using RegRipper's "compname" plugin.
| Value    | Result    |
| --- | --- |
|  ComputerName   |  DESKTOP-SKPTDIO   |
|  TCP/IP Hostname   |     |

### 🔍 Finding: The system identifies itself as DESKTOP-SKPTDIO on the network.

### 3. Operating System Version Analysis

#### Current Windows Version

| Field    | Value     |
| --- | --- |
|  ProductName   |  Windows 10 Home    |
|  ReleaseID   |   2009   |
|  BuildLab   |     |
|  CurrentBuild  |     |
|  InstallDate   |      |
|  RegisteredOwner   |  Patrick    |

### Previous Windows Version

| Field    | Value     |
| --- | --- |
|  ProductName   |  Windows 10 Home    |
|  ReleaseID   |   2009   |
|  BuildLab   |     |
|  CurrentBuild  |     |
|  InstallDate   |      |


#### Physical Evidence of Previous Installation:

* Windows.old folder exists at C:\Windows.old
  
* This folder is automatically created when Windows is upgraded or reinstalled while preserving the previous installation

#### 💡 Key Finding: The system was upgraded/reinstalled on the same day (January 10, 2022), preserving the previous installation in Windows.old. Both current and previous installations are Windows 10 Home (Build 22000).

### 4. Time Zone Configuration

| Field    | Value     |
| --- | --- |
|  TimeZoneKeyName   |  Eastern Standard Time    |
|  Bias   |   2009   |
|  DaylightName   |     |
|  StandardName  |     |
|  LastWrite Time   |      |


#### 🔍 Finding: The system is configured for Eastern Time Zone (UTC-5). All timestamps in this report should be interpreted with this time zone context.


### 5. Connected Mobile Device Analysis

### Evidence Summary

| Source    | Finding    |
| --- | --- |
|  USB Device Attached (Autopsy)   |  Apple, Inc. - iPhone 5/5C/5S/5E    |
|  USB Enumeration (Registry)   |  VID_05C8&PID_0815 with device identifiers   |
|  Connection Times   |  First: 2022-02-03 21:05:48 PST   |
|                      |   Last: 2022-02-12 14:47:31 PST           |

### USB Device Details

| Field    | Value     |
| --- | --- |
|  Manufacturer  |  Apple, Inc.   |
|  Model   |   iPhone 5/5C/5S/5E  |
|  Device ID   |     |
|  Parent ID Prefix  |     |
|  First Install Date   |      |
|  Last Arrival   |      |

#### ✅ Confirmed: An Apple iPhone (5 series) was connected to this Windows computer on multiple occasions between February 3-12, 2022.








