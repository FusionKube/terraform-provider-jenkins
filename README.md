# Terraform Provider

- Website: https://www.terraform.io

This is a community provider and is not supported by Hashicorp.

## Installation

This provider has been published to the Terraform Registry at https://registry.terraform.io/providers/FusionKube/jenkins. Please visit the registry for documentation and installation instructions.

## Developing the Provider

Working on this provider requires the following:

* [Terraform](https://www.terraform.io/downloads.html) 1.0+
* [Go](http://www.golang.org) (version requirements documented in the `go.mod` file)
* [Docker Engine](https://docs.docker.com/engine/install/) 20.10+ (for running acceptance tests)

You will also need to correctly setup a [GOPATH](http://golang.org/doc/code.html#GOPATH), as well as adding `${GOPATH}/bin` to your `$PATH`.

To compile the provider, run `make`. This will install the provider into your GOPATH and print instructions on registering it into your system.

In order to test the provider, you can simply run `make test`.

```sh
$ make test
```

In order to run the full suite of Acceptance tests, run `make testacc`. These tests require Docker to be installed on the machine that runs them, and do not create any remote resources.

```sh
$ make testacc
```

When changing a data source or resource, you may need to update the documentation. This documentation is automatically rendered by https://github.com/hashicorp/terraform-plugin-docs. To trigger a render, execute:

```sh
$ make generate
```

## Attribution

This provider is inspired from the work of https://github.com/ramadhan25/terraform-provider-jenkins and https://github.com/ringanta/terraform-provider-jenkins. Most of the codes and documentations are copied from there.
