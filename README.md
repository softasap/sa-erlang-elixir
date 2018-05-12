sa-erlang-elixir
================

[![Build Status](https://travis-ci.org/softasap/sa-erlang-elixir.svg?branch=master)](https://travis-ci.org/softasap/sa-erlang-elixir)

Installs erlang language (https://www.erlang.org/) and, optionally, elixir (http://elixir-lang.org/).


Erlang is a general-purpose, concurrent, functional programming language. It is also a garbage-collected runtime system. The sequential subset of Erlang supports eager evaluation, single assignment, and dynamic typing.

Elixir is a dynamic, functional language designed for building scalable and maintainable applications.

Elixir leverages the Erlang VM, known for running low-latency, distributed and fault-tolerant systems, while also being successfully used in web development and the embedded software domain.

Example of usage (all parameters are optional)

Simple

```YAML
  roles:
    - {
        role: "sa-erlang-elixir"
      }
```

Advanced:


```YAML
  roles:
    - {
        role: "sa-erlang-elixir",
        option_install_elixir: false,
        erlang_package: erlang,
        erlang_additional_packages: []  
      }
```




See https://www.erlang-solutions.com/resources/download.html for details

1. What is the erlang package?
Erlang/OTP Platform is a complex system composed of many smaller applications (modules). Installing the erlang package automatically installs the entire OTP suite. Since some of the more advanced users might want to download only a specific selection of modules, Erlang/OTP has been divided into smaller packages (all with the prefix erlang-) that can be installed without launching the erlang package.
2. What is esl-erlang, how is it different from erlang? Have you removed it from repositories?
The esl-erlang package is a file containg the complete installation: it includes the Erlang/OTP platform and all of its applications. The erlang package is a frontend to a number of smaller packages. Currently we support both erlang and esl-erlang.
Note that the split packages have multiple advantages:
seamless replacement of the available packages,
other packages have dependencies on erlang, not esl-erlang,
if your disk-space is low, you can get rid of some unused parts; erlang-base needs only ~13MB of space.


Usage with ansible galaxy workflow
----------------------------------

If you installed the `sa-erlang-elixir` role using the command


`
   ansible-galaxy install softasap.sa-watchman
`

the role will be available in the folder `library/softasap.sa-erlang-elixir`
Please adjust the path accordingly.

```YAML

     - {
         role: "softasap.sa-erlang-elixir"
       }

```




Copyright and license
---------------------

Code is dual licensed under the [BSD 3 clause] (https://opensource.org/licenses/BSD-3-Clause) and the [MIT License] (http://opensource.org/licenses/MIT). Choose the one that suits you best.

Reach us:   

Subscribe for roles updates at [FB] (https://www.facebook.com/SoftAsap/)

Join gitter discussion channel at [Gitter](https://gitter.im/softasap)

Discover other roles at  http://www.softasap.com/roles/registry_generated.html

visit our blog at http://www.softasap.com/blog/archive.html
