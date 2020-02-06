# Osama Al Banna Resume

#### Last Update Date : 2020/01/23
Please Use [this](https://mega.nz/#F!21QzFAYb!YDFikLBkTp0KznPFZU68mQ) decrypted mega link to download/show the resume

Please Notice : To protect this file from any manipulation i signed it
* Internally with : Foxit Phantom
  * To check it press on the signature at the right bottom corner of this page (may not working on the browser)
  
* [Externally With : GPG](https://www.phildev.net/pgp/gpginstall.html)
  * [Signature File : named [this file name].pdf.sig](https://www.thesecuritybuddy.com/pgp-and-gpg/digital-signature-using-gpg/)
  * My Fingerprint : `3C0CF524B1AE5C08D2CF1576CB13D5ABD30D7F9A`

### Open Source Projects

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
  * Demonstrate Very Complex Topics In Functional Programming , with javascript


### Private Projects
  * Some projects can not published as a public repository to github now so i will provide a preview for those projects
  * Every project link leads to preview `video` on mega cloud provider

### Projects Previews

#### [ActiveBook](https://mega.nz/#!r4AFySYa!7Ba4twziL4mBpZZtIlyoyk4hfkTnrbtI3JP328ATZmQ)

##### Social Network App
##### built as demonstration of hyper clean arch

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
            `this pattern must use with only awareness developers, not suitable for intermediate level or begineer developer`
            since this may leads to issues with testing (FDD/BDD) if developers does not know how to controlling its side effects
    * To Respect SC we delegate validation out of ef core to Command or Query in CQRS `MediatR`
        * we use `FluentValidation.AspNetCore` package to support popular validation, and created our custom validation
    * All Loading of nested entities done with `LazyLoadingProxies` middleware to prevent loading non necessary data
        * For that we use `AutoMapper` without needing to configure it with ef core, since all loading be lazy
    * All Mapping With `AutoMapper` Package `DI EF CORE` version
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

</p>
</details>

<details><summary>Frontend Technologies </summary>
<p>

* [React](https://reactjs.org/)
  * UI manager 
* [Typescript](https://www.typescriptlang.org/)
  * Type safty enhancer
* [Axios](https://github.com/axios/axios)
  * HTTP client
* [mobx-react-lite](https://mobx-react.js.org/)
  * State mangament system
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

##### [PHP CMS](https://mega.nz/#F!SxokwCzJ!k1LbVXZuluso6IKNfYsiVA)
  * Content Management System
  * Technologies
    * PHP : `Pure 7.1`
     * Sessions : `Used Apache Server Sessions , No Client Session, Only cokie with id`
    * [Jwt](https://github.com/firebase/php-jwt) : `AuthSystem Base`
    * `Every Server Side Functionalities Built from scratch except jwt generator`
    * MySql
    * Bootstrap 4
    * Files Prvider : Local File System
  * Notes
    * This application demnostrate the main design paradigm php oriented to , which called/ImplementedAs `Spaghetti Pattern`
      * This Pattern considered as an `anti-pattern` , so it's very dangerous to use it in medium+ application
      But since it is the most commom paradigm php designed for 
      `for example you can use many globals/statac variable at any place` which violate SRP `Single Responsibility Principle`
    * So, Why Create This app with this pattern ?
      * Answer : to demonstrate some of use cases of this pattern , and show how very easy this pattern may destroy any project
     with just simple refactoring
     
     * At the end , there is no way in php to implement things like Clean Architecture without top-level abstraction layers
     eg, frameworks `eg, laravel` to restrict some of the language features or produce an alternatives of anti-pattern core features ,`but surely this will comes with performance costs`


##### [DateBook](https://mega.nz/#F!SxpigCRK!OcOXxDvfqRPZvVOwJH-XTQ)
  * Dating Social App
  * Use Next Technologies
    * Backend : Asp.net Core Web API  `3.0 => 3.1`
    * Frontend Container : Angular8
    * UI Helpers : ngx-bootstrap
    * Sqlite & SqlServer
    * Files Prvider : Cloud
      * [Cloudinary](https://cloudinary.com)
  * Patterns
    * Based On repository pattern
    * Respect Modularitys & SOLID Design Principles

 
#### [GraniteHouse](https://mega.nz/#F!6oIhyCbJ!sw7SwcJ79-bWvN9rIQBOIQ)
   * Granite Trading Site
   * Technologies
     * Asp.net Core MVC : 2.1
     * Razor Pages `For Registeration System`
     * SqlServer
     * * Files Prvider : Local File System
     
#### [AbtWifiPassUI](https://mega.nz/#!exJRVK5a!-kvdJX0QLk9uvTGry1_tIa8PwNo2sNgJy0UFekZvbSo)
  * UI Utils Allow to fetch all saved wifi passwords from local machine
  * developed with wpf & windows system sdk
  * [Silent Version](https://mega.nz/#!LsJ3HIpD!vOMtRkZwN8gDLZo0W3DikKYmPr_AZiskCYb5h8YHomw) : `fetch password list in by just click on exe file and save it to exe location`
    * developed with windows form
    
  ![wpUI](./previews/AbtWifiPassUIPreview.gif)

#### [Wpf Simple Store Manager](https://mega.nz/#!S9QRxYgQ!54FHe9rOf3spao3U-pf0F35E50N4cazykYAxF1hm5EQ)
   * The main purpose of this app is demonstrate using pointers between different windows without losing data in wpf app
   * Technologies
     * Wpf
     * SqlServer & SQLite
