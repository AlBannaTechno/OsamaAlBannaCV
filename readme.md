# Osama Al Banna Resume

##### Note: Some of next projects base ideas inspired by popular success busniss projects or online training course/s

### Public Commercial Projects

#### Installments Manager (مدير الأقساط)
This application is another story in Desktop Application Industry
It used new exclusive `private` technologies, to make everything reactive and reusable


This app orinted around [DDD](https://www.dddcommunity.org/)


### Update, Released: [Link](https://albannatechno.github.io/InstallmentsManagerProject/README)

I will publish a snaps from the code and github issue trackers, once the application finished

<details><summary>Screenshots</summary>
<p>

 ### UPDATE: RELEASED INFO `Current`
 
 ![2021-03-20_190536](https://user-images.githubusercontent.com/13814190/120482478-7ab14e00-c3b1-11eb-9949-11ecd7d17980.png)

 ### PRE-RELEASE INFO `Old`
 
![2021-03-20_190536](https://user-images.githubusercontent.com/13814190/111878098-5e576500-89af-11eb-8482-772f459e6225.png)



I still have some issues to solve, and some features to implement, before publish the first final release
![2021-02-04_153113](https://user-images.githubusercontent.com/13814190/106899681-53e25400-66fe-11eb-8b5c-93ea6d84d17c.png)

Click the image to zoom

![2021-03-20_19-09-45](https://user-images.githubusercontent.com/13814190/111878263-31578200-89b0-11eb-9f3b-acfff6133ae3.png)

Project Diagram

![2021-02-04_154438](https://user-images.githubusercontent.com/13814190/106901452-71b0b880-6700-11eb-9a64-427362f94f06.png)

This project like some others, based on well organized exlusive `personal` nuget packages

the packages this project uses

![106902484-935e6f80-6701-11eb-877b-f14005a04b952](https://user-images.githubusercontent.com/13814190/110095524-b1250000-7da5-11eb-8c99-0806ba031e57.png)

</p>
</details>


#### [NetConto](https://www.youtube.com/watch?v=DfJW_CvYl2I)
  * `The Most Advanced Network Throttling And Monitoring Application`
  * This Application Is Unique
  * Written in
     * C/C++: for low level network controlling, and driver programming based on *npf*
     * C# .net for managed code
     * WPF for layout
     * NoSql Embeded Db *LiteDB*
     * low level code connected to .net via low level interpolotion and un managed .net code `& un safe`

#### [NetMonto](https://www.youtube.com/watch?v=3SlsOuEPcfI)
  * `The Most Advanced Network Throttling And Monitoring And Controlling Application`
  * This App Can Control Everything in your network, even how much data user can consume per minute/day/....
  * This Application Is Unique, and it is the enterprise version of <b>NetConto</b>
  * Written in
     * The same as *NetConto*
     * Build Completly in Reactive Programming including UI   
### Open Source Projects

#### [C# Design Patterns Collection](https://github.com/AlBannaTechno/C-Sharp-Design-Pattern-Collection)
  * `Contains an implementations for most of design patterns in C# language`

#### [BanMvc](https://github.com/AlBannaTechno/BanMvcZero)
  * `PHP MVC Framework That Porting Some Of [C# Asp.net Core] Features, philosophies To PHP`

#### [FriendOrganizer](https://github.com/AlBannaTechno/FinalFriendsOrganizer)
  * `Wpf Friend Organizing Application Build With Advanced Enterprise Technologies `
  * Can used as a core of any dynamic high performance desktop application with .net

#### [AbtTerminal](https://github.com/AlBannaTechno/AbtTerminal)
  * `Embedded terminal project based on Pyqt`

#### [AlBannaDesigner-OpenGL](https://github.com/AlBannaTechno/AlBannaDesigner-OpenGL)
  * `Graphic Engine With OpenGL/C++`

#### [AbtNumericalSystemConverter](https://github.com/AlBannaTechno/AbtNumericalSystemConverter)
  * `Numerical System Converter with any base & support Command Line Interface `

#### [NwJsDefinitelyTyped](https://github.com/AlBannaTechno/NwJsDefinitelyTyped)
  * `DefinitelyTyped files to support autocomplete and embedded docs for NwJs Projects`

#### [Gravity-center-and-Area-Calculatore](https://github.com/AlBannaTechno/Gravity-center-and-Area-Calculatore)
  * `Calculate Center Of Gravity And Area Of 3D Shapes With Drwaing it in 2d/3d with Orthographic/Perspective`
  * Built with pyqt/opengl/glfw3

#### [JsAreaCalculater](https://github.com/AlBannaTechno/AreaCalculater)
  * `Calculate Area With (x,y) points by divide it as triangles`
  * Demonstrate Advanced Scenarios In Functional Programming , with javascript


### Private Projects
  * Some projects can not published as a public repository to github now so i will provide a preview for those projects
  * Every project link leads to preview `video` on mega cloud provider

### Projects Previews

#### [ActiveBook](https://mega.nz/#!r4AFySYa!7Ba4twziL4mBpZZtIlyoyk4hfkTnrbtI3JP328ATZmQ) → [Album](https://myalbum.com/album/fdYYG8X973792F/)

![ActiveBookPreview mp4_20210629_182508 301](https://user-images.githubusercontent.com/13814190/123842427-0cf53500-d911-11eb-830b-c4c70f493185.jpg)

##### Social Network App For Activities
##### built as demonstration of hyper clean arch
##### Notice, in preview we used 500ms delays for every http request to simulate response delays.

<details><summary>Backend Technologies</summary>
<p>

* Asp.net Core
* Architecture
    * [Clean Arch](https://docs.microsoft.com/en-us/dotnet/architecture/modern-web-apps-azure/common-web-application-architectures#clean-architecture)
        * With Hyper Separation Of Infrastructure Layers
        * Communication With CQRS
            * Implemented With MediatR Pattern as MediatR.net Package
    * Both Client Side And Server Side Respect All Solid Principles
        * except store part of client side since using DI(IoC) with react/mobx is just an overhead
            so we use self-referencing `God Object` anti pattern
            * this pattern `anti` can be used safely with some restrictions in dynamic typing languages
            * since this may leads to issues with some of testing methodologies (FDD/BDD)`@ subcutaneous test, UI test` if developers does not know how to controlling its side effects

    * To Respect SCP we delegated validation out of `entity framework core` to Command or Query in CQRS `MediatR`
        * we use `FluentValidation.AspNetCore` package to support popular validation, also created some custom validations
    * All Loading of nested entities done with `LazyLoadingProxies` middleware to prevent loading non necessary data
        * For that we use `AutoMapper` without needing to configure it with ef core, since all loading be lazy
    * All Mapping With `AutoMapper` Package `Dependency.Injection.CORE` version
    * Notes
        * We Delegate any logic out of Domain Layer, so domain only have models
            * and as known in testing , `Domain models are not application entities`
            so Model is a pure `POCO` object
* Database
    * Developing `sqLite`
    * Production
        * `SqlServer` for Azure
        * `MySql/MariaDB` for Linux Server
* VCS
    * GitHub

* Cloud Providers
    * Cloudinary For Image storage and images manipulation eg,`Focus cropping to face`
* RealTime & MultiCasting Communications
    * SignalR

</p>
</details>

<details><summary>Frontend Technologies </summary>
<p>

* [React](https://reactjs.org/)
  * UI manager
* [Typescript](https://www.typescriptlang.org/)
  * Type safety enhancer
* [Axios](https://github.com/axios/axios)
  * HTTP client
* [mobx-react-lite](https://mobx-react.js.org/)
  * State management system
* [semantic-ui-react](https://react.semantic-ui.com/)
  * Layout/UI Components
* [react-router-dom](https://reacttraining.com/react-router/)
  * Routing System Provider/Controller
* [react toastify](https://fkhadra.github.io/react-toastify/)
  * Toasting Messages
* [react final form](https://final-form.org/docs/react-final-form/getting-started)
  * Form Wrapper
* [revalidate](https://github.com/jfairbank/revalidate)
  * Prebuilt validations for form fields

</p>
</details>


<details><summary>Project Structure</summary>
<p>


* Domain
    * Contains all domain entities projects
    * Zero Local Dependency

* Application
    * Contains all business logic projects
    * Depends on
        * Domain
        * Persistence

* API
    * Contains Web API projects
    * Responsible for receiving and responding to http requests
    * Depends on
        * Application

* Persistence
    * Contains Persistence projects
    * Responsible for database access and queries
    * Depends on
        * Domain

* Infrastructure
    * Local
        * Contains local infrastructure projects eg, IoC, Security, Interfaces
    * Remote
        * Contains remote infrastructure project eg, Cloud repositories for images and videos

* Presentation
    * Contains UI/Client projects eg, reactApp , angularApp ...
    * But Not Asp.net Core MVC App `This project is web api & client`
    * Ignored by default from .git of backend to allow work separately on front-end

* Dev
    * For any development files
    * Ignored from git track

</p>
</details>

<details><summary>Architecture Diagrams</summary>
<p>

#### Calls UML Diagram

![wpUI](./previews/ActiveBook/FinalCalls.png)

#### References UML Diagram

![wpUI](./previews/ActiveBook/FinalReferences.png)

</p>
</details>

#### [PHP CMS](https://mega.nz/#F!SxokwCzJ!k1LbVXZuluso6IKNfYsiVA)
##### Content Management System

<details><summary>Technologies</summary>
<p>

* PHP : `Pure 7.1`
 * Sessions : `Used Apache Server Sessions , No Client Session, Only cokie with id`
* [Jwt](https://github.com/firebase/php-jwt) : `AuthSystem Base`
* `Every Server Side Functionalities Built from scratch except jwt generator`
* MySql
* Bootstrap 4
* Files Provider : Local File System


</p>
</details>

<details><summary>Notes</summary>
<p>

* This application demonstrate the main design paradigm php oriented to , which called/ImplementedAs `Spaghetti Pattern`
  * This Pattern considered as an `anti-pattern` , so it's very dangerous to use it in medium+ application
  But since it is the most common paradigm php designed for
  `for example you can use(access/modify) many global/static variables from anywhere in the code` which violate SRP `Single Responsibility Principle`
* So, Why Create This app with this pattern ?
  * Answer : to demonstrate some of use cases of this pattern , and show how very easy this pattern may destroy any project
 with just simple refactoring

 * At the end , there is no way in php to implement things like Clean Architecture without top-level abstraction layers
 eg, frameworks `eg, laravel` to restrict some of the language features or produce an alternatives of anti-pattern core features ,`but surely this will comes with performance costs`


</p>
</details>


#### [DateBook](https://mega.nz/#F!SxpigCRK!OcOXxDvfqRPZvVOwJH-XTQ) - ِ[Album](https://myalbum.com/album/DHCV4fDm5LCekF/)

![DateBookReviewHQ75 mp4_20210629_182318 536](https://user-images.githubusercontent.com/13814190/123844236-1089bb80-d913-11eb-9aea-02b84c41164f.jpg)

##### Dating Social App

<details><summary>Technologies</summary>
<p>

* Backend : Asp.net Core Web API  `2.2 => 3.0`
* Frontend Container : Angular8
* UI Helpers : ngx-bootstrap
* Sqlite & SqlServer
* Files Provider : Cloud
  * [Cloudinary](https://cloudinary.com)

</p>
</details>

<details><summary>Patterns</summary>
<p>

* Based On repository pattern
* Respect Modularity & SOLID Design Principles

</p>
</details>

#### [GraniteHouse](https://mega.nz/#F!6oIhyCbJ!sw7SwcJ79-bWvN9rIQBOIQ)
##### Granite Trading Site

<details><summary>Technologies</summary>
<p>

* Asp.net Core MVC : 2.1
* Razor Pages `For Registeration System Layout`
* SqlServer
* Files Provider : `Local File System`

</p>
</details>

#### [Python Tkinter library to make any widget overlayed on the screen](https://www.youtube.com/watch?v=o297gigXWAA)
##### Can used to handle overlayed widgets of any application without messing with the application logic

<details><summary>Details</summary>
<p>

* Used Python Tkinter as a GUI Library
* Allow any widget or window to be on top/top-most and allow click through via alpha chanel
* Highly Customizable if needed, but it can work directly without any additional configuration
* Handle Clicks 
* Optionally override the widget geastures
* Drag and Drop
* Customizable z-index depth visability

</p>
</details>


#### [AbtWifiPassUI](https://mega.nz/#!exJRVK5a!-kvdJX0QLk9uvTGry1_tIa8PwNo2sNgJy0UFekZvbSo)
##### UI Utils Allow to fetch all saved wifi passwords from local machine

<details><summary>Details</summary>
<p>

* [UI Version](https://mega.nz/#!exJRVK5a!-kvdJX0QLk9uvTGry1_tIa8PwNo2sNgJy0UFekZvbSo)
  * developed with wpf & windows system sdk
* [Silent Version](https://mega.nz/#!LsJ3HIpD!vOMtRkZwN8gDLZo0W3DikKYmPr_AZiskCYb5h8YHomw)
   * `fetching passwords list by just clicking on exe file and save it to exe location`
   * developed with windows form
* Note
  * I remove tracking keyboard via remote server functionality since it is not encrypted and most of antivirus software
  will treat it as a malicious software
    * this happens because this functionality based on execute `memory injection` attack from C++ dll via unsafe code
    so you need to encrypt the source code and only compile it on the flay, so i will need to ship gcc compiler with
    this app, since neither me or you have a certification to publish this application with it and we can not legally
    accomplish this, so i just decide to move it to my rates software repository `private`.
    * Also still need to chip `gcc` or `g++` with `the spy server` to allow low level execution , and this will only
    work well with windows xp, vista, `unless you have a vulnerability to melt this app process with it :)`

    * Also you should know , this mechanism is very popular in `RAT` applications `eg, njRAT`.

</p>
</details>

<details><summary>Preview</summary>
<p>

![wpUI](./previews/AbtWifiPassUIPreview.gif)

</p>
</details>



#### [Wpf Simple Store Manager](https://mega.nz/#!S9QRxYgQ!54FHe9rOf3spao3U-pf0F35E50N4cazykYAxF1hm5EQ)
#### The main purpose of this app is demonstrate using pointers between different windows without losing data in wpf app

<details><summary>Technologies</summary>
<p>

 * Wpf
 * SqlServer & SQLite

</p>
</details>

#### For more projects: take a look at [AlBannaTechno Account](https://github.com/AlBannaTechno/)
