# Spring PetClinic on TAP 

This project is a fork of the famous Spring PetClinic application.

[See this page](https://github.com/spring-projects/spring-petclinic)
if you need more details about this application.

Using this repository, you can deploy the PetClinic app to
[VMware Tanzu Application Platform](https://tanzu.vmware.com/application-platform),
your platform simplifying the Kubernetes developer experience.

No need to mess with Dockerfile or craft kilometers of YAML files, you can now deploy
PetClinic to your favorite Kubernetes distribution with a single command.

## How to use it?

Use this command to deploy the app:

```shell
tanzu apps workload apply -f config/workload.yaml
```

<img width="1042" alt="petclinic-screenshot" src="https://cloud.githubusercontent.com/assets/838318/19727082/2aee6d6c-9b8e-11e6-81fe-e889a5ddfded.png">

### Binding this app to PostgreSQL

Use this command to deploy a PostgreSQL database:

```shell
tanzu service class-claim create spring-petclinic-db --class postgresql-unmanaged --parameter storageGB=1
```

You can now deploy the app including the PostgreSQL configuration:

```shell
tanzu apps workload apply -f config/workload-postgres.yaml
```

### Binding this app to MySQL

Use this command to deploy a MySQL database:

```shell
tanzu service class-claim create spring-petclinic-db --class mysql-unmanaged --parameter storageGB=1
```

You can now deploy the app including the MySQL configuration:

```shell
tanzu apps workload apply -f config/workload-mysql.yaml
```

# Contributing

The [issue tracker](https://github.com/spring-projects/spring-petclinic/issues) is the preferred channel for bug reports, features requests and submitting pull requests.

For pull requests, editor preferences are available in the [editor config](.editorconfig) for easy use in common text editors. Read more and download plugins at <https://editorconfig.org>. If you have not previously done so, please fill out and submit the [Contributor License Agreement](https://cla.pivotal.io/sign/spring).

# License

The Spring PetClinic sample application is released under version 2.0 of the [Apache License](https://www.apache.org/licenses/LICENSE-2.0).

[spring-petclinic]: https://github.com/spring-projects/spring-petclinic
[spring-framework-petclinic]: https://github.com/spring-petclinic/spring-framework-petclinic
[spring-petclinic-angularjs]: https://github.com/spring-petclinic/spring-petclinic-angularjs 
[javaconfig branch]: https://github.com/spring-petclinic/spring-framework-petclinic/tree/javaconfig
[spring-petclinic-angular]: https://github.com/spring-petclinic/spring-petclinic-angular
[spring-petclinic-microservices]: https://github.com/spring-petclinic/spring-petclinic-microservices
[spring-petclinic-reactjs]: https://github.com/spring-petclinic/spring-petclinic-reactjs
[spring-petclinic-graphql]: https://github.com/spring-petclinic/spring-petclinic-graphql
[spring-petclinic-kotlin]: https://github.com/spring-petclinic/spring-petclinic-kotlin
[spring-petclinic-rest]: https://github.com/spring-petclinic/spring-petclinic-rest
