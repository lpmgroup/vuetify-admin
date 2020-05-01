<p align="center">
<a href="https://laravel.com" target="_blank" rel="noopener"><img src="https://user-images.githubusercontent.com/3679080/79393326-6758de80-7f75-11ea-9196-8ecf990b40fd.png" width="300"></a>
</p>

<p align="center">
<a href="https://www.npmjs.com/package/vtec-admin"><img src="https://img.shields.io/npm/v/vtec-admin.svg?style=flat-square" alt="Latest Version on NPM"></a>
<a href="https://www.npmjs.com/package/vtec-admin"><img src="https://img.shields.io/npm/l/vtec-admin.svg?style=flat-square" alt="License"></a>
</p>

# Vtec Admin

SPA admin library for Vue.js running on top of REST APIs, built on Vuetify and comes with dedicated Vue CLI plugin for 🚀. Ready to use on Laravel API backend by using official [Vtec Laravel Crud](https://github.com/okami101/vtec-laravel-crud) composer package, but can be used on every backend of your choice with your own data and authentication providers.

> See [full documentation](https://vtec.okami101.io)  
> Check [online demo](https://vtec-bookstore-demo.okami101.io/admin) -> use prefilled login (read only)  
> Note : this project is heavily inspired by [React Admin](https://github.com/marmelab/react-admin/) made by awesome [Marmelab Team](https://marmelab.com/)

[![sc](https://user-images.githubusercontent.com/3679080/80732263-58913080-8b0c-11ea-9074-56668c44a876.png)](https://vtec-bookstore-demo.okami101.io/admin)

## Features

* Powered by Vuetify, and come with nice [Material Theme by Creative Tim](https://github.com/creativetimofficial/vuetify-material-dashboard).
* Full standalone UI SPA admin that can be adapted to any backend (REST, GraphQL, SOAP, etc.) by writing your own data and auth providers by following specific contracts which ensure compatibility.
* Bare minimal Vue.js code needed to get your CRUD pages working, while allowing limitless customization.
* If using Vue CLI project (heavily recommended), [Vue CLI plugin](https://www.npmjs.com/package/vue-cli-plugin-vtec-admin) will be your ideal companion by installing all minimal boilerplate code for insane quick start. Can be used on any Vue.js based application as well.
* 100% Vue CLI friendly. Vtec Admin is simply a plugin which integrates within all of your existing plugins, notably Vue Router, Vuex and Vuetify. Keep total control of your Vue app by adding your own routes with custom pages, custom store modules, and full Vuetify theming as you are used to on Vue CLI base project.
* Ready to use data and auth providers for Laravel.
* Cookie based authentication auth provider for [Laravel Sanctum](https://github.com/laravel/sanctum). If you prefer JWT instead, simply write your own provider that follow specific auth contract.
* Advanced permissions.
* Official [Vtec Laravel Crud](https://github.com/okami101/vtec-laravel-crud) provided for insane quick start from top to bottom. Provide many backend features as spa authentication, profile editing, users management, impersonation, [translatable fields](https://github.com/spatie/laravel-translatable), [media support](https://github.com/spatie/laravel-medialibrary), [file manager](https://github.com/Studio-42/elFinder) with Wysiwyg bridges, etc.
* Associate to Laravel Crud and CLI plugin, Vtec Admin allows you immediate start developement from backend to UI with already basic functional admin.
* Stay as little magic as possible by fully respecting each backend and frontend development environnement. If you know well Laravel and Vue CLI basics, so you're ready to go !
* CRUD code generators are offered on both Laravel backend and Vue frontend for even quicker ready-to-go API and UI with basic CRUD boilerplate code generation. Each can be totally used separatly.
* With combination of Vtec Admin DSL, code generators as well as Vue.js power, feel the better mix between productivity and limitless customization.
* Full featured bookstore demo application, with [Laravel backend](examples/laravel) running on Docker and his associated [Vue CLI admin project](examples/demo) using [Vtec Admin](packages/admin).
* Complete documentation.
* Internationalization support via Vue I18n, with full english and french translations provided. Can be easily configured by taking user browser language.
* Translatable resource fields by contextual language selection on each crud page.
* Unique v-model context by form for minimal boilerplate code.
* Server-side form validation support.
* Autocomplete input with entity reference support.
* TinyMCE 5 as default Wysiwyg with elFinder bridge, can be replaced by your own.
* Full-featured datagrid, including multi-sort, pagination, global search, advanced filters, basic CSV export, live query string context. And of course with possibility of cell templating.
* Data iterator decoupled from datagrid which allows you total customization of list layout.
* Advanced filters as-you-type with many inputs: select, boolean, autocomplete for search by relations, with multiple, etc.
* Customizable by-row, bulk and global actions.
* Direct aside create/edit from list instead of separate crud page.
* Many fields and inputs components for various data types: select, enums, boolean, number, rich text, etc.
* To finish, for what it's worth, it's completely free.

## But why another admin panel again

### Main goals

* Nice ready-to-go Vuetify UI theme.
* SPA admin which deliver complete Vue.js power admin development.
* Full backend independence by using low-level auth and data providers.
* [DSL](https://en.wikipedia.org/wiki/Domain-specific_language) approach, minimal boilerplate code for best development experience with as little magic as possible.
* Powerful code generators for highest productivity.
* Best balance between productivity and customization.
* Maximize usage by thoughtful combination of many opensource projects.

The main goal of Vtec Admin is to get you rid off all CRUD boilerplate code that can be very nasty on full SPA Admin. Very bare minimal Vue.js code is needed to get your Vue CRUD pages working with standard nice basic layout. On the other side, with combination of Vue.js component power development, you have limitless customization at hand. This is sort a Vue.js equivalent to [React Admin](https://github.com/marmelab/react-admin/), which uses [DSL](https://en.wikipedia.org/wiki/Domain-specific_language) approach.

### Place of this project within other admin frameworks

So many admin panel are generaly tightly coulpled with backend framework and prevent us to switch easily. Besides most of the time it stays classic server-side templating engine oriented associated to good old jQuery plugins, with no usage of a powerfull UI framework as Vue.js. I think notably on [Backpack](https://backpackforlaravel.com/) on Laravel (not free) and free [EasyAdmin](https://github.com/EasyCorp/EasyAdminBundle) for symfony world. The main advantage of this admin panels is to be highest productive as possible (and plently featured in case of Backpack) but tends to come with her own logic and stay first of all very configuration oriented.

On the other side, the official [Laravel Nova](https://nova.laravel.com/) is a very productive Vue SPA admin, with obviously big community, but not free, still Laravel-coupled and come with his own caveats (you tend to follow the "Nova" way for specifics needs with unnatural mix of coupled PHP and Vue development).

[React Admin](https://github.com/marmelab/react-admin/) (RA) is by far the most cool and customizable admin panel i ever seen. It's totally free and really independent of any backend. Althought it isn't clearly the more efficient way to build administrable app from top to bottom with backend included, this is in my opinion the true way to build admin apps, just as LEGO&copy; !

But I'm a Vue.js fan and I didn't find a close equivalent based on it. So why not to try a make one, mainly for "fun" and hard training ?

### The case of backend API

By its nature, RA doesn't propose any helpers for backend framework. [Api Platform Demo](https://github.com/api-platform/demo) does awesome work for Symfony area, although it's an very extreme approach of minimal boilerplate, which leads to more magic and harder to extend. Moreover it's come with Hydra guessers for even less code on UI side as default which is not very suitable for real app in my opinion.

So I choose to make a [complete helper package](https://github.com/okami101/vtec-laravel-crud) for Laravel in order to have the best quick start experience possible, combined to generators for high productivity, while highly respecting the pure Laravel way to make CRUD resources. Absolutly no magic but damn good old YAML based code generators, similar as [Blueprint](https://github.com/laravel-shift/blueprint), with less features to confess.

## Simplified architecture

![Simplified architecture](diagrams/architecture.svg)

## State

> This is a really alpha state package, use it only for adventure !

Many of RA existing features has been transposed in this project, but without some of them as client-side data cache and optimistic UI which necessit many work for something i don't really need. Besides this feature turn-off server-side validation which i'm not really a fan of it.  
Contrary to RA, no specific API-side lazy or eager relationships fields was included for list and show views, because more efficient directly on server-side with far less code. It's ok if you have full control of backend.

This app is of course far to be as sharp as RA which the admin panel I highly recommended you to use for business apps, besides I didn't write a single test...  
Moreover RA has really fast growing contributions and tends to be the "de facto" standelone SPA admin.

More backend showcase examples as Symfony / NestJS / Spring Boot / ASP.NET Core in addition to existing Laravel would be nice but it asks really too much work for now, especially when if I must develop a dedicated composer / npm / maven / NuGet packages for each...

> As this project was made on my free time and is totally free and open-source, don't expect any support of anything. This project was just mainly a personal challenge and only aims to satisfy my own needs on personal projects. For real production on essential sites I strongly advise you to go with [React Admin](https://github.com/marmelab/react-admin/) which is far more mature.

## Note on this main repo

This main repo contains all necessary projects to develop Vtec Admin and run demo :

* [Vtec Admin Library](packages/admin), the main admin library.
* [Vtec Admin Vue CLI Plugin](packages/cli), the associate Vue CLI plugin which contains all base code boilerplate for quick install and commands code generator.
* [Vtec Laravel Crud](vtec-laravel-crud), git submodule of composer package to use on fresh Laravel project which facilitates Vtec Admin integration and includes server-side commands generator.
* [Bookstore Admin Demo](examples/demo), full-featured admin sample build on top of main Vtec Admin Library.
* [Bookstore Laravel Demo](examples/laravel), suitable API backend for previous bookstore admin demo based on Laravel.
* [Tutorial Admin Demo](examples/tutorial), finished tutorial after following [dedicated docs](https://vtec.okami101.io/tutorial) which aims to made a good showcase of YAML code generation power.
* [Vtec Docs](packages/docs), vuepress docs.

All of this projects are automatically linked together by symlinks (thanks to yarn workspaces and composer) for best library development experience in this project. HMR from demo to admin library side-by-side is fully supported !

## Usage

### How to run demo locally

Be sure to have clone this repo with git submodules.  
If not use `git submodule init && git submodule update`. [Vtec Laravel Crud](vtec-laravel-crud) should be cloned.

Docker is required for quick-start run backend API. If you don't want it, follow [dedicated instructions](examples/laravel#docker).

Use Makefile for easy starting all necessery tools.
For Windows users just install [scoop](https://scoop.sh/) and `scoop install make`

Use `make help` for all detail commands.

In order to run demo :

```bash
make install # intall all yarn dependencies
make run-laravel-demo # run server api through docker (take a coffee if 1st time...)
make prepare-laravel-demo # initialize laravel app and inject dummy data (use it only at 1st launch)
make run-demo # compile all bookstore demo admin with HMR dev mode enabled
```

Admin panel should be autostart to [http://localhost:8080](http://localhost:8080)

### Run and build docs

Docs are build with VuePress. Use `make run-docs` to launch it and `make build-docs` for build it info static files inside "docs" repo root folder.

## Similar inspiring projects

### Backend-free admin panel builder

* [React Admin](https://github.com/marmelab/react-admin/), by far the most cool and customizable SPA admin panel, and totally free and independent of any backend. Just build admin panel as LEGO&copy; ! But not the most productive as is (no backend helpers), and highest learning curve compare to the others. Can be even cooler if used within [Api Platform](https://github.com/api-platform/api-platform) for backend.

### Free Symfony classic admin panel

* [EasyAdmin](https://github.com/EasyCorp/EasyAdminBundle), standard admin builder, not many widgets by default but very efficient and heavily configurable by YML config files and extendable with twig templates.
* [Sonata Admin](https://github.com/sonata-project/SonataAdminBundle), super massive admin builder, maybe one of the most powerful and full featured free admin panel on the market, but not really a seamless development experience.

### Some Laravel admin panels

* [Backpack](https://backpackforlaravel.com/), not free for commercial projects, old school HTML jQuery and come with quickly bloated code in case of specific custom development needs, but still stay one of the most productive admin panel on the market with a tons of widgets.
* [Official Laravel Nova](https://nova.laravel.com/), not free and the most expensive, but full featured and very efficient SPA admin builder for Laravel with Vue.js. Code as fast as Backpack but with modern UI Framework and nice Laravel-ish development experience.
* [Voyager](https://voyager.devdojo.com/), free admin panel available for Laravel.

## Full documentation

Full documentation can be found on the [Vtec docs website](https://vtec.okami101.io).

## License

This project is open-sourced software licensed under the [MIT license](https://adr1enbe4udou1n.mit-license.org).
