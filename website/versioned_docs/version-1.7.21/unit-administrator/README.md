---
id: version-1.7.21-README
title: Unit Administrator's Guide
sidebar_label: Unit Administrator's Guide
original_id: README
---

It is a document for people who want to manage pre-built Personium Unit and those who want users to use PDS applications to provide PDS service using Personium  

For those who build Personium Unit, and how to build / deploy / configure Personium server programs, please refer to [Server Software Operator's Guide](../server-operator/README.md).

## Unit User and Unit level API

Unit User is a user who is issued a Unit User Token recognized by the Personium Unit and is a main entity capable of operating Unit level API such as CRUD of Cell.

* [Unit User](./Unit-User.md)

Unit User Token (UUT) is required for access to the Unit level API, which manages cell generation and management.
In addition, Cell remembers which UUT was generated when it was created, and always grants privileged access to all APIs at Cell level and Box level for Unit User who created them.

## Tutorial

We have released a tutorial on basic operations for managing Personium Unit.
If you are the first person to manage Personium Unit please check.

* [Create Cell Tutorial](./tutorial.md)

## Management of Unit using GUI

By using the following Unit manager GUI, almost all API access can be implemented as a Unit User.

[app-uc-unit-manager](https://github.com/personium/app-uc-unit-manager)

This tool supports multiple launch methods, and when launched from the Home application of the User Cell, it starts up in the form of the URL of the target cell to be accessed and token information for access as a startup parameter.
In that case, this application behaves as a Cell Manager. On the other hand, especially when such a parameter is not specified, Start up as Unit manager GUI.

## Cell Creator sample GUI

Using the Unit Manager GUI above, you can try various API operations manually, but it would be unrealistic for Unit administrators to manually add records to Cell Publishers.

In many cases, you will need to create a program to create Cell with the prescribed specifications, create a cell usage application screen, and so on. In that case please use the sample application below.

[app-uc-cell-creator](https://github.com/personium/app-uc-cell-creator)

For small-scale operation, you can use this sample program itself to pay out Cells.

## Other

* [Data management](./Data_Management.md)

## Related Repositories
* [app-uc-unit-manager](https://github.com/personium/app-uc-unit-manager)
* [app-uc-cell-creator](https://github.com/personium/app-uc-cell-creator)
