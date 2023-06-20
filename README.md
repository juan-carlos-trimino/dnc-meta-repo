# dnc-meta-repo
A project using .NET Core/C# with Linux containers

This is a demo on how to use .NET Core/C# in a Linux environment. The demo consists of five repos using RabbitMQ, Redis, and two S3 clients (written in C# and Go) using blog storage.

To download all repos, please execute the command below:<br>
```
$ meta git clone https://github.com/juan-carlos-trimino/dnc-meta-repo.git
```

You will need the following to successfully deploy the application:<br>
- [Terraform](https://www.terraform.io/) - Infrastructure as Code (IaC).
- [Meta](https://github.com/mateodelnorte/meta) - To track multiple repositories as a single aggregate repository thereby making the management of multiple repositories easier.
- A cluster.
- S3 storage.

Finally, if you are running the demo on **RedHat OpenShift**, you will need to do the following:
- Requires to use the RedHat image for the .NET Core runtime.
- Add the following line to the **.csproj** file:<br>
  ```
  <PropertyGroup>
    …
    <RuntimeIdentifier>rhel-x64</RuntimeIdentifier>
    …
  </PropertyGroup>
  ```
