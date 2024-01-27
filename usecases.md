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

![uml sequence diagram for use case #001](src/usecases/001-create-contacts-list.svg)

## 002 - Share contacts list


**Inputs**:

- 

**Outputs**:

- 1x encrypted contacts list URL
- 1x public key

---

![uml sequence diagram for use case #002](src/usecases/002-share-contacts-list.svg)

## 003 - View shared contacts list



**Inputs**:

- 1x encrypted contacts list URL
- 1x public key 

**Outputs**:

- 1..* contact record

---

![uml sequence diagram for use case #003](src/usecases/003-view-shared-contacts-list.svg)

## 004 - Save contacts list



**Inputs**:

- 

**Outputs**:

- 

![uml sequence diagram for use case #004](src/usecases/004-save-contacts-list.svg)

## 005 - Import contacts list



**Inputs**:

- 

**Outputs**:

- 

![uml sequence diagram for use case #005](src/usecases/005-import-contacts-list.svg)
