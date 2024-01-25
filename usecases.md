# usecases

This document keeps track of all use cases the project aims to deliver, including their description, requirements, scope and availability.

---

|Use Case|Scope|Integrated in|
|--------|-----|-------------|
|001 - Create contacts list|`User`|`Alpha`|
|002 - Share contacts list|`User`|`Alpha`|
|003 - View shared contacts list|`Viewer`|`Alpha`|
|004 - Save contacts list|`User`|`Alpha`|
|005 - Import contacts list|`User`|`Alpha`|

---

## 001 - Create contacts list

This use case enables the creation of a contacts list. The input must be a list of contact records and the output shall be a pair of **private** and **public** keys, as well as the link to where contacts have been saved.

**Inputs**:

- 1..* contact record

**Outputs**:

- 1x private key
- 1x public key
- 1x encrypted contacts list URL

---

![uml sequence diagram for use case #001](src/usecases/001-list-advertised-jobs.svg)

## 002 - Share contacts list

This use case is executed through the platform search bar. The goal is to let te user search for jobs in a free-manner, being guided with an autocomplete feature. The output shall be a list of jobs advertised by retails that fit the user input.

**Inputs**:

- 1x Job name query

**Outputs**:

- 0..* advertised jobs

---

![uml sequence diagram for use case #002](src/usecases/002-search-jobs.svg)

## 003 - View shared contacts list

This use case is available if use case [#002](#002---search-for-a-job) is executed and returns more than **15** jobs. The goal is to allow the user to refine his job search in quick manner. The possible filters are:

- location (city)
- payment method
- field of expertise
- cost

**Inputs**:

- 0..* applied filters

**Outputs**:

- 0..* advertised jobs

---

![uml sequence diagram for use case #003](src/usecases/003-filter-listed-jobs.svg)

## 004 - Save contacts list

This use case can be executed in two ways. The first one is directly on the job listing and shall provide a quick preview of the advertised job (**description**, **pricing**, **availability**). The second way is clicking the "I'm interested" button, which shall redirect the user to a page with all the details of the job, as well as reviews.

**Inputs**:

- 1x job

**Outputs**:

- 1x job details

![uml sequence diagram for use case #004](src/usecases/004-see-details-about-advertised-job.svg)

## 005 - Import contacts list

This use case is all about reaching to the retailer who has published the job. Contacting can be done externally through the retailer phone number and socials like WhatsApp, Facebook Messenger, and more. The use can be triggered directly from the job listing or in the details page.

**Inputs**:

- N/A

**Outputs**:

- N/A

![uml sequence diagram for use case #005](src/usecases/005-contact-job-retailer.svg)

## 006 - Leave review on advertised job

This use case can only be executed after the user gets the job done. The retailer must notify internally that the job was done, generating an unique **link** that will allow the user to provide feedback about the job. The user can receive this link via **e-mail**, **message** or the retailer can show a **QR Code** that the user can scan.

**Inputs**:

- 0..1 Text feedback
- 1x rating (1-5)
- 1x Unique feedback link

**Outputs**:

- 1x Job review

![uml sequence diagram for use case #006](src/usecases/006-leave-review-on-advertised-job.svg)

## 007 - Share advertised job on social media

This use case is pretty simple: users are invited to share a job they found interesting in social media. Sharing platforms include **Facebook**, **Instagram**, **WhatsApp**, **Twitter** and **Threads**.

**Inputs**:

- 1x Advertised job
- 1x Social media platform

**Outputs**:

- N/A

![uml sequence diagram for use case #007](src/usecases/007-share-advertised-job.svg)

## 008 - Create retailer profile

This use case allows retailers to identify themselves on the platform. The retailer must include information such as his **name**, **description**, **location**, **contacts**, **preferred payment methods**, **fields of operation** and **social media accounts**.

**Inputs**:

- 1x Retailer name
- 1x Retailer description
- 1..* Location
- 1..* Contact
- 1..* Preferred payment methods
- 1..* Fields of operation
- 0..* Social media accounts

**Outputs**:

- 1x Retailer profile

![uml sequence diagram for use case #008](src/usecases/008-create-retailer-profile.svg)

## 009 - Publish job advertisement

This use case allows a retailer to publish a job advertisement. The retailer must include information such as the job **name**, **description**, **field**, **availability**, **cost** and **location**. The retailer must be **authenticated** to execute this use case.

**Inputs**:

- 1x Job name
- 1x Job description
- 1x Location
- 1x Cost
- 1..* Availability
- 1..* Fields of operation
- 1..* Payment methods

**Outputs**:

- 1x Advertised job

![uml sequence diagram for use case #009](src/usecases/009-publish-job-advertisement.svg)