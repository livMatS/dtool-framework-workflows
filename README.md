# dtool-framework-workflows

Copyright 2022 Johannes Hoermann, johannes.hoermann@imtek.uni-freiburg.de

## Introduction

This repository provides reusable CI workflows for components of the dtool ecosystem, i.e. for

* `livMatS/dserver` [on dockerhub](https://hub.docker.com/r/jotelha/dserver), [on github](https://github.com/livMatS/dserver-container-image)
* `livMatS/dtool-lookup-client` [on dockerhub](https://hub.docker.com/r/jotelha/dtool-lookup-client), [on github](https://github.com/livMatS/dtool-lookup-client-container-image)
* `livMatS/dtool-token-generator-ldap`[on dockerhub](https://hub.docker.com/r/jotelha/dtool-token-generator-ldap), [on github](https://github.com/livMatS/dtool-token-generator-ldap-container-image)
* https://github.com/livMatS/dserver-container-composition

## Development

This repository is the top layer in our dtool ecosystem CI. From top to bottom, those layers are

* [`dtool-framework-workflows`](https://github.com/livMatS/dtool-framework-workflows) (this repositry), in paricular `.github/workflows/dtool-lookup-framework-generic-container-image-build-and-test.yml`
  * [`dserver-container-composition`](https://github.com/livMatS/dserver-container-composition)
    * actual containers (see *Introduction* above)
      * dtool Python packages at https://github.com/jic-dtool and https://github.com/livMatS.

In case of modifications and bumped versions in a lower layer, propagate step-by-step through layers above.
