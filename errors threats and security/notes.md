# Errors, Threats and Security

## Sources of Errors

1.  Human Errors

    > The security of a computer system can be compromised by human errors, which can occur at various levels:

    -   GIGO (Garbage In, Garbage Out) :
        -   This principle states that the quality of output is determined by the quality of input. If incorrect or poor-quality data is entered into a system, it will lead to erroneous outputs.
    -   Input Errors:
        -   Incorrect data entry, misconfigurations, or misunderstanding of system requirements.

2.  Arithmetic Errors

    -   Rounding Errors :
        -   Occur when numbers are rounded during calculations, leading to inaccuracies.
    -   Overflow and Underflow :
        -   Overflow occurs when a calculation exceeds the maximum limit of a data type, while underflow happens when a number is too small to be represented.
    -   Precision Errors :
        -   Occur when floating-point numbers cannot accurately represent certain values, leading to small discrepancies in calculations.
    -   Truncating :
        -   Involves cutting off digits after a certain point, which can lead to loss of precision.

3.  Data Transmission Errors

    > Data is sent in packets from one computer to another, either using wired or wireless connections. Errors can occur during this transmission process, affecting the integrity of the data being sent.

    -   Errors during data transmission can occur due to various factors, including:
        -   Noise in the communication channel.
        -   Signal degradation over long distances.
        -   Interference from other electronic devices.
        -   Hardware malfunctions.

4.  Programming Errors

    > A program can contain various types of errors, including:

    -   Syntax Errors:
        -   Mistakes in the code that violate the programming language's rules, preventing the program from running.
    -   Logic Errors:
        -   Flaws in the program's logic that lead to incorrect results or behavior, even if the code runs without crashing.
    -   Runtime Errors:
        -   Errors that occur while the program is running, often due to unexpected conditions or inputs.

## Solutions for Errors

### Verification

Data verification is the process of ensuring that data is accurate and complete. It involves checking the data against predefined criteria or rules to confirm its validity. Can be compared to ascertain its **completeness**, **correctness**, and **consistency**.

### Validation

Validation is the process of checking whether the data meets the required standards or criteria before it is processed or used. It ensures that the data is suitable for its intended purpose and adheres to specific rules or formats. In a program, the user can be prompted to re-enter data until it is valid, or the program can assign default values if the input is invalid.

| Check                            | Description                                                                                                                      | Example                                                                                   |
| -------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| Presence                         | The data must exist and not be empty                                                                                             | A field that cannot be left blank (a required field)                                      |
| Range                            | The data must fall within a specified range                                                                                      | A number that must be between 1 and 100                                                   |
| Uniqueness                       | The data must be unique and not duplicated                                                                                       | A username that cannot be used by another user                                            |
| Length                           | The data must have a specific length                                                                                             | A password that must be at least 8 characters long                                        |
| Type                             | The data must be of a specific type                                                                                              | An email address that must follow a specific format                                       |
| Format                           | The data must follow a specific format                                                                                           | A date that must be in the format YYYY-MM-DD                                              |
| Logical                          | The data must make sense logically                                                                                               | A start date that cannot be after an end date                                             |
| Check digit                      | The data must have a valid check digit                                                                                           | A credit card number that must pass the Luhn algorithm                                    |
| Check sum                        | Verifies the integrity of data by ensuring that the sum of its parts matches a predetermined value                               | A file that must have a checksum to verify its integrity                                  |
| Data transmission check - Parity | Ensures that the number of bits with a value of 1 in a binary representation is even or odd, depending on the parity scheme used | A byte that must have an even parity bit set to ensure data integrity during transmission |

### Techniques for input

> The best way to control input is to force the user to key in as little as possible. The more characters the user has to key in, the more likely they are to make a mistake.

1. Keyboard Input
    > Common but prone to typign errors
2. Barcode Sanner
    > Fast and accurate for stock systems.
3. QR Codes
    > Store large amounts of data, quick scanning.
4. GUI Components
    > Dropdowns, checkboxes, and radio buttons reduce input errors by limiting choices.
5. RFID Tags
    > Used for inventory and asset tracking, allowing quick identification without manual input.
6. Biometric Input
    > Fingerprint or facial recognition for secure access, reducing the risk of unauthorized input.
7. OCR
    > Optical Character Recognition for digitizing printed text, reducing manual data entry errors.

## Database Management System Integrity

Accuracy

> Accuracy is the degree to which the stored value measures against the true value. For example the number of decimal places in a number.

Correctness

> Data is correct if it confirms to an approved or conventional standard or agreeing with fact, logic, or known truth.

Currency

> Currency is the degree to which the data is up to date. For example, a database of customers that has not been updated for a year may not be current.

Completeness

> Completeness is the degree to which all required data is present. For example, a database of customers that does not include their email addresses may not be complete.

Relevance

> Relevance is the degree to which the data is applicable to the current situation. For example, a database of customers that includes their purchase history may be more relevant than one that does not.

## Threats to Computer Systems

### SQL Injection

SQL Injection is a code injection technique that exploits a security vulnerability in an application's software by inserting or "injecting" malicious SQL statements into an entry field for execution. This can allow attackers to manipulate the database, retrieve sensitive data, or even execute administrative operations.

Example:

```sql
SELECT * FROM users WHERE username = 'admin' OR '1'='1';
```

This query would return all users in the database because the condition '1'='1' is always true, allowing unauthorized access.

Or if they wanted to delete all users:

```sql
SELECT * FROM users WHERE username = 'admin'; DROP TABLE users; --';
```

### Hardware Failure

Hardware failure refers to the malfunction or breakdown of physical components of a computer system, such as hard drives, memory, or power supplies. This can lead to data loss, system crashes, and downtime.

#### Storage

Hard drive crashes are one of the most frustrating hardware failures. They can result in the loss of all data stored on the drive, including important files, applications, and system settings. Regular backups and using redundant storage solutions can help mitigate this risk.

#### Power Failure

Power failures can cause abrupt shutdowns, leading to data corruption and potential hardware damage. Using uninterruptible power supplies (UPS) can help protect against sudden power loss and allow for safe system shutdowns.

### Malware

Malware, short for malicious software, is any software intentionally designed to cause damage to a computer, server, client, or computer network. It can take various forms, including viruses, worms, trojans, ransomware, spyware, and adware.

#### Phishing and Spoofing

Phishing is a technique used by attackers to trick users into revealing sensitive information, such as usernames, passwords, or credit card numbers, by masquerading as a trustworthy entity. This is often done through emails or websites that appear legitimate but are designed to steal user data.

Spoofing involves impersonating a legitimate user or system to gain unauthorized access or information. This can include email spoofing, where the sender's address is forged, or IP spoofing, where the source IP address of a packet is altered.

#### Virus

A virus is a type of malware that attaches itself to legitimate programs or files and spreads from one computer to another when the infected program is executed. Viruses can corrupt or delete data, slow down system performance, and cause other harmful effects.

#### Trojan Horse

A trojan horse is a type of malware that disguises itself as a legitimate application or file to trick users into installing it. Once installed, it can create backdoors for attackers, steal sensitive information, or perform other malicious actions without the user's knowledge.

#### Spyware

Spyware is software that secretly monitors user activity and collects information without the user's consent. It can track browsing habits, capture keystrokes, and gather personal data, often leading to privacy violations and identity theft.

#### Pharming

Pharming is a cyber attack that redirects users from legitimate websites to fraudulent ones without their knowledge. This is often done by compromising the DNS (Domain Name System) settings or exploiting vulnerabilities in web browsers, leading users to enter sensitive information on fake sites.

#### Ransomware

Ransomware is a type of malware that encrypts a user's files or locks them out of their system, demanding a ransom payment to restore access. It can cause significant disruption and financial loss, as victims may be forced to pay the ransom or lose their data permanently.

### Denial of Service Attacks

#### DoS Attack

A DNS attack targets the Domain Name System (DNS), which translates human-readable domain names into IP addresses. By compromising DNS servers or manipulating DNS records, attackers can redirect users to malicious websites, intercept communications, or disrupt internet services.

#### DDoS Attack

A **D**istributed **D**enial **o**f **S**ervice attack

### Wi-Fi Vulnerabilities

## Security Solutions

### RAID

**R**edundant **A**rray of **I**nexpensive **D**isks **(RAID)** uses two or more hard disks so that if one hard drive fails the other hard drive(s) on the server will contain a copy of the data providing a reliable hard drive storage. _RAID is not a backup facility; It is protection against hard drive failure_

#### RAID Level 1

Level 1 uses **mirroring** in which all data is stored on two hard disks simultaneously (the one being a mirror image of the other), but data is only accessed from one main hard disk with the second kept as a backup.

#### RAID Level 5

RAID level 5 uses disk **striping** with parity which requires a minimum of three hard disks. Data is written in _"stripes"_ across the three hard drives with no one disk having the same data.

RAID level 5 offers better performance than mirrorring and is cheaper per megabyte.

However if one fails disk access will be slow as the data must be reconstructed from the other drives.

![imabge](http://blog.everycity.co.uk/wp-content/uploads/2008/10/raid5.png)

### Backup

A copy of the data is placed in a secure space such as offsite or an external drive

page 113 for onsite and remote backup.

### Uninterruptible Power Supply

(UPS) is an electrical device that provides emergency power to electrical equipment when the normal power source fails.
