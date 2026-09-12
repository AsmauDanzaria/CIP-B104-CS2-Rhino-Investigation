# CIP-B104-CS2-Rhino-Investigation
Digital forensic investigation of the CIP-B104 Rhino Possession case study.

## Overview

This repository contains my submission for CIP-B104 Case Study 2, based on the historical Rhino Hunting / Illegal Possession digital forensics case.

The investigation involved the examination of a USB forensic image and three network captures. The work included USB file recovery, steganography analysis, FTP and HTTP reconstruction, encrypted archive recovery, hash-based deduplication and static examination of a recovered Windows executable.

## Investigation Summary

The examination identified four unique rhino images from the USB evidence.

FTP reconstruction recovered `rhino1.jpg`, `rhino3.jpg` and an encrypted archive containing `rhino2.jpg`. Hash comparison showed that `rhino2.jpg` was identical to an image already recovered from the USB.

HTTP analysis recovered two additional unique rhino images, `rhino4.jpg` and `rhino5.gif`.

A JPEG file was also confirmed as containing JPHide-embedded data. Although the passphrase was recovered, the concealed payload could not be completely extracted and validated as an image.

After hash comparison and deduplication, eight unique rhino images were independently validated from the available evidence.

## Main Areas Covered

- Evidence preservation and integrity verification
- FAT16 filesystem examination
- File carving with PhotoRec
- Hash-based duplicate identification
- Steganography detection
- JPHide password recovery
- FTP traffic reconstruction
- Encrypted ZIP recovery
- HTTP object reconstruction
- Static PE executable analysis
- UTC timeline reconstruction
- Cross-source evidence correlation

## Tools Used

The investigation used tools including:

- md5sum
- sha256sum
- Sleuth Kit
- fsstat
- fls
- icat
- PhotoRec
- ExifTool
- stegdetect
- stegbreak
- JPSeek
- TShark
- capinfos
- fcrackzip
- 7-Zip
- file
- xxd
- strings
- objdump

## Repository Contents

The submission ZIP contains the assessment report and supporting investigation material, including:

- PDF report
- command and code records
- forensic reports
- screenshots
- timeline records
- correlation and deduplication records
- relevant recovered and exported derivatives

The original evidence supplied by the Academy is not included.

## Evidence Handling

The original forensic evidence was preserved and examined using verified working copies where appropriate.

Recovered credentials and passwords were treated as sensitive information and were redacted from the final submission material.

The recovered Windows executable was examined using static techniques only and was not executed.

## Student

**Name:** Asmau Danzaria  
**Registration Number:** 2617285  
**Course:** CIP-B104
