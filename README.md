# Vuex at Scale

Some ideas (and boilerplate) about managing medium/large apps with Vue, Vuex and
API calls.

## Main ideas

* API calls must not be directly coupled to Vue (or any other framework, FWIW).
  Separation of Concerns.
* Specific http requests library (such as axios in this example) should be
  provided as a dependency to our services, so it is easily mocked.
* A 1:1 mapping between services and API endpoints is strongly encouraged. This
  way, frontend and backend will share a common language to talk about data.
  IMHO any solution without this benefit is a suboptimal solution.
* Vuex Store should use modules and namespaces.

## Things not covered by this repo

* Authentication.
* Storing all your data in Vuex or requesting directly from your components is a
  project-specific decision. However, I'd suggest using Vuex by default. You
  could even use Vue Router.
* Error management. This repo provides no solution to this, since every project
  will manage them in a particular way.
* Data validation and normalization (a.k.a. data formatting before passing it
  down to components from Store).



## Scripts

As usual:

```
npm install
```

```
npm run serve
```

```
npm run lint
```

```
npm run test:unit
```
