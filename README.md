# Visual Pathing Algorithms Specification (tentative name)

## Alexander Giammaruti

## September 2020

## 1 Introduction

## 1.1 Purpose

This software requirements specification is intended to lay out the foundation for the requirements
necessary for the development of my personal project to visually represent pathing algorithms in an
accessible way for educational and reference purposes. This will be the first version of said application and
will be releasing as build 1.0 when it has reached the requirements of functionality outlined in this
document. This specification will outline further details about the processing restrictions, acceptance
criteria, and all other sufficient information to support all major design strategies. Finally this document is
intended ultimately to serve as a guiding hand to keep the programmer (me) within the given scope of the
project, and to possibly be used in future interviews as a show of professionally when even producing my
own personal work.

## 1.2 Document Conventions

The conventions followed in the specification document include formatting by IEEE standards as well as
some typographical term conventions outline below:

- IDE, in this document refers to the ’Integrated Development Environment’ that I will use for most of
    the applications development
- TOS, in this document refers to the ’Terms of Service Agreement’ each user will have to attest to an
    agreement to use the freely provided software within the provided limits placed by myself, the code
    monkey who made it.
- Authentication, in this document refers to the act of logging in to this web application using a unique
    username and a secret password
- Authorization, in this document refers to the permissions granted to user accounts upon registration.
- Administrator, in this document refers to myself. As a single man ”development team” any errors or
    problems should be reported to myself at any time during specification, design, implementation, or
    any time after first launch. I will be able to authorize Users (see below) to register for the web
    application with a username and password after agreeing to a brief TOS
- User, in this document refers to any other users of the software whom are registered to authentication
    with a username and password, and has the ability to save any path diagrams they have constructed
    up to a certain memory limitation.
- Starting Point, in this document refers to the beginning point on a grid to represent where a pathing
    algorithm will originate
    (also referred to as:P 0 −Pn)
- Ending Point, in this document refers to the point on a grid meant to denote where a path is desired
    to end by a user. If ending points past the initial ending pointE 0 , it will become the new starting
    pointP 1 and search forE 1. This process will continue untilEnis reached.
    (also referred to as:E 0 −En)


### 1.3 Intended Audience and Reading Suggestions

The formal intended audience for this specification is myself and any who are interested in the development
process and/or the final products defined specifications. This specification is subject to change in future as
issues with certain portions may be met in later stages of development. these sections will be denoted as
’edited ¡date & time¿’. Proceeding this introductory chapter, there will be four additional chapters in
which I will illustrate the overall description of the software, external interface requirements, system
features, and other non-functional requirements; in that order. It is suggested that section 1.2:
Document Conventions is among the first read portions of this specification as it will provide
the necessary definitions for terms used throughout this specification.Beyond these conventions,
the chapters and content have been organized in a suggested lexicographic order for reading.

### 1.4 Project Scope

—eventual-name-of-software— is a software designed to be used freely as an education or reference tool by
any reputable organization, student, or individual whom may find it useful at any point. Therefore at any
given point past first implementation the scope could be minimal or could be very large.

### 1.5 References

IEEE’s digital library was used to obtain the template for which this specification was created with; slight
modifications were made. The template document can be downloaded through the following link:
IEEE specification template

## 2 Overall Description

### 2.1 Project Perspective

My software project, —eventual-project-name—, is envisioned as a useful tool to understand the
innerworkings of pathing algorithms and (after initial development completion) possibly other types of
algorithms as well. This software will provide a visual representation of different algorithms running based
upon constraints placed on the initial starting ’grid’. This will show their complexities visually with a
breakdown of their run-time efficiencies depending on the initial constraints.

### 2.2 User Classes and Characteristics

2.2.1 Admin

- add/remove users
- update or recover user info

2.2.2 User

- request authorization to become registered user
- log in/ log out
- save starting points created to a defined limit
- delete starting points saved to database
- report bugs, errors, or other anomalous behavior to the admin

### 2.3 Operating Environment

As a web application this software will be available for use in any browser given the necessary performance
requirements


### 2.4 Design and Implementation Constraints

This project must be developed as a web application to allow for almost infinite portability. This software
is meant to be used in a variety of places through a variety of devices ranging from desktop to mobile
phone, and must be constructed to be presented well through all these possible form factors.

### 2.5 User Documentation

A general use guide/ manual will be provided within the web application for new users, possibly with a
repeatable tutorial to familiarize new users with the use case of the web application

### 2.6 Assumptions and Dependencies

It is assumed users will have some browser capable device to access the web application through. The
ongoing use of the web application will require a constant connection to the internet.

## 3 External Interface Requirements

### 3.1 User Interfaces

One general user interface will be developed. A re-sizable grid to place constraints on with which selected
algorithms will find the shortest path between a starting and an ending point. dropdown menus and/ or
other means of selection will be available in a ’top-bar’ to choose between what types of cells are to be
drawn on the graph, what algorithm will be used to determine path, endpoint behavior, and other various
means of user control for start conditions.

### 3.2 Software Interfaces

- —undecided SQL server system—
- —Angular7+ framework—
- —undecided web-hosting—

## 4 System Features

### 4.1 Authentication and Authorization

4.1.1 Description and Priority

Login security is vital to ensure the integrity of user authorization. Users should be able to access their
saved data and only their saved data. As a principle, Authentication and Authorization are paramount in
priority in even silly projects I create, as it is important in industry. Therefore I consider thishighpriority

4.1.2 Stimulus/ Response Sequences

Upon launch of the application users must provide login credentials to access their saved data. Otherwise
the application can be used entirely without authentication or authorization.

4.1.3 Functional Requirements

REQ-1: Device must be browser capable
REQ-2: Internet connection is required to use this application
REQ-3: Database to ensure login information is unerring.
REQ-4: Graphic User Interface that can present information and fields in an appropriate way.
ACT-1: Application will inform the user if there is a lack of internet connection.
ACT-2: Application will inform the user if the credential information input is imprecise.


### 4.2 Storage of Users’ Starting-Point Data

4.2.1 Description and Priority

Users will be able to store starting conditions to a certain memory constraint to be determined during
development. Additionally the user if they so choose will also have the option to remove saved starting
conditions to make room if their storage has filled. As this is not crucial for initial development, User data
storage is ofmediumpriority

4.2.2 Stimulus/ Response Sequences

Users will be prompted with the option upon selecting a save button, or attempting to navigate away with
unsaved data. Similarly a delete button will be available allowing users to select which of their saved
starting conditions they wish to remove from saved storage.

4.2.3 Functional Requirements

REQ-1: Device must be browser capable
REQ-2: Internet connection is required to use this application
REQ-3: Database to ensure login information is unerring.
REQ-4: Graphic User Interface that can present information and fields in an appropriate way.
ACT-1: Application will inform the user if there is a lack of internet connection.
ACT-2: Application will inform the user if the credential information input is imprecise.

## 5 Other Nonfunctional Requirements

### 5.1 Performance Requirements

A Marginally powerful computer with internet access and a browser

### 5.2 Security Requirements

Users may log in to save and retrieve saved starting conditions, but authentication and authorization are
not needed to use the basic features.

### 5.3 Software Quality Attributes

Portability is the primary necessity of this project. The desire is to be able to use this application on a
variety of devices connected to a browser (within reason). I.E. a desktop, smartphone, tablet, etc... This is
why a web application is to be used for implementation as it allows for almost unlimited portability of my
product.

