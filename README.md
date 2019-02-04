# 0-docker-intro
Intro to docker materials to support lunch and learn

## Getting Started
1. cd into mynginx
1. ./build.sh
1. ./run.sh
1. http://localhost:8080
1. ./stop.sh

## Build child image
1. cd into mynginxcustom
1. ./build.sh
1. ./run.sh
1. http://localhost:8080
1. ./stop.sh

## Compare layers
1. from repo root dir ...
1. ./inspect_layers
_Note the layer reuse._

## Modify parent image
1. cd into mynginx
1. cp index.html2 index.html
1. ./build.sh
1. ./run.sh
1. http://localhost:8080
1. ./stop.sh

## Compare layers
1. from repo root dir ...
1. ./inspect_layers
_Note the layers are different._

## Test child image
1. cd into mynginxcustom
1. ../run.sh
1. http://localhost:8080
_Note nothing has changed._
1. ./stop.sh
1. ./build.sh
1. ./run.sh
1. http://localhost:8080
_Note the extra line is now present._
1. ./stop.sh

## Compare layers
1. from repo root dir ...
1. ./inspect_layers
_Note the layer reuse again._
