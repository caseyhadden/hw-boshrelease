An attempt at creating a 'Hello world' type of BOSH release...

The goal of this BOSH release is to land a single executable file as a package
which is referenced by a job and started by BOSH.

That executable is built from the go-http-helloworld repository. The blob is
included here for convenience.

You should be able to:

1. Clone this repository
2. Run bosh create release --force
3. Run bosh upload release
4. Run bosh-gen manifest hw-dev
5. Run bosh deploy
6. curl http://host:8888

and then get back a hello world response.

This BOSH release has a single property to specify the port to listen for HTTP
requets on. This defaults to 8888.

Package and job files in this repository were initially populated via the
bosh-gen gem.
