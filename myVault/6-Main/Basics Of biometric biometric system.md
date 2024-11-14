
tag : [[Biometrics]]

## Benefit of biometric biometric system

|       **Benefit**        | **Explanation**                                                                                                                                                                                                             |
| :----------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|    Increased Security    | - Biometrics provide a higher level of security by ensuring access only for authorized users.  <br>- Passwords and PINs can be guessed; tokens can be stolen.  <br>- Biometrics data cannot be guessed or stolen as easily. |
|  Increased Convenience   | - Passwords are often simple for ease of memory, leading to vulnerability.  <br>- Biometrics are unique to individuals and difficult to forget.  <br>- Reduces need for multiple passwords or tokens.                       |
| Increased Accountability | - Biometrics allow strong auditing, eliminating practices like buddy-punching.  <br>- Provides certainty about who accessed what and when.  <br>- Presence of auditing can act as a deterrent to unauthorized access.       |


## Operation of a biometric system
#### Main Modules : 
- Sensor module
- Quality assessment and feature extraction module
- Matching and decision-making module
- System database module


##### Sensor module :-
- A suitable biometric reader or scanner is required to acquire the rawbiometric data of an individual.
##### Quality assessment and feature extraction module 
- The quality of the biometric data acquired by the sensor is firstassessed in order to determine its suitability for further processing.
- Typically, the acquired data is subjected to a signal enhancementalgorithm in order to improve its quality. However, in some cases, thequality of the data may be so poor that the user is asked to presentthe biometric data again
- During enrollment, this feature set is stored in the database and iscommonly referred to as a `template`


##### Matching and decision-making module
- The extracted features are compared against the stored templates to generate match scores.


## Biometric characteristics
- **Universality**: Every individual accessing the application shouldpossess the trait. 
- **Uniqueness** : The given trait should be sufficiently different acrossindividuals comprising the population. 
- **Permanence**: The biometric trait of an individual should be sufficiently invariant over a period of time with respect to the matching algorithm. A trait that changes significantly over time is nota useful biometric.
- **Measurability**: It should be possible to acquire and digitize thebiometric trait using suitable devices that do not cause undueinconvenience to the individual.

## Stages in Biometrics system
### Enrollment
- A biometric system is trained to identify a specific person. 
- The person first provides an identifier, such as an identity card. • The biometric is linked to the identity specified on the identification document. 
- The distinctive features are located and one or more samples are extracted, encoded, and stored as a reference template for future comparisons 
- Template size varies depending on the vendor and the technology.
- Templates can be stored; remotely in a central database or within a biometric reader device itself
### Verification Stage
- In the verification mode, the system validates a person’s identity by comparing the captured biometric data with her own biometric template(s) stored in the system database

### Identification Stage

- In the identification mode, the system recognizes an individual bysearching the templates of all the users in the database for a match


| **Feature**                  | **Verification System**                            | **Identification System**                               |
| ---------------------------- | -------------------------------------------------- | ------------------------------------------------------- |
| **Purpose**                  | Confirms if a person is who they claim to be       | Determines a person’s identity among many in a database |
| **Comparison Process**       | Matches data against an individual's existing data | Compares data against multiple entries in the database  |
| **Computational Power**      | Requires less computational power                  | Requires more computational power                       |
| **Speed**                    | Faster, often completes in less than one second    | Slower, due to multiple comparisons                     |
| **Accuracy**                 | Higher accuracy for single matches                 | May reduce accuracy due to more possible false matches  |
| **Use Case**                 | Access control, user authentication                | Duplicate enrollment elimination, identifying unknowns  |
| **Decision Type**            | Match/No-Match with a specific identity            | Determines if the person is in the database             |
| **Duplicate Presence Check** | Cannot identify if a person exists multiple times  | Can identify if a person is enrolled multiple times     |



## Types of Templates

- Enrolment Templates
- Match templates



## Scoring
- `-1` to `1`



## Accuracy in Biometric Systems


### False match rate, (FMR)
- A biometric solution’s false match rate is the probabilitythat a user’s template will be incorrectly judged to be a match for a differen user’s template
- The false match rate is often referred to as the `false acceptance rate(FAR)`.
- False match rate and false nonmatch rate are `inversely related` and must always be assessed


### False Nonmatch Rate(FNMR)
- (FNMR) is the probability that a user’s template will be incorrectly judged to not match his or her enrollment template
### Failure-to-Enroll (FTE) Rate 
- A system’s failure-to-enroll (FTE) rate represents the probability that a given user will be unable to enroll in a biometric system


### Relation of Failure-to-Enrol to False Nonmatch Rate

$$FMR=1/FNMR$$

### Ability-to-Verify (ATV) Rate

$$
ATV=(1-FTE)(1-FNMR)
$$


