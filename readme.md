# Maven Signed Deployment Action

Builds and deploys Maven artifacts to Github.

## Inputs

| Input      | Description                                                             | Required                              |
|------------|-------------------------------------------------------------------------|---------------------------------------|
| token      | Github security token.                                                  | True                                  |
| repository | Maven repository (distribution management) for deploying the artifacts. | False, defaults to 'ossrh'            |
| profile    | Maven profile for site deployment.                                      | False, defaults to 'deployment-ossrh' |
| jdk        | JDK version to use.                                                     | False, defaults to '11'               |

## Usage

This builds and deploys the Maven site.

```yaml
jobs:
  deploy:
    name: Deployment
    runs-on: ubuntu-latest

    steps:
    - name: Deploy signed
      uses: bernardo-mg/maven-github-deployment-action@v1
      with:
        token: ${{ secrets.token }}
        username: ${{ secrets.username }}
        password: ${{ secrets.password }}
```

## Collaborate

Any kind of help with the project will be well received, and there are two main ways to give such help:

- Reporting errors and asking for extensions through the issues management
- or forking the repository and extending the project

### Issues management

Issues are managed at the GitHub [project issues tracker][issues], where any Github user may report bugs or ask for new features.

### Getting the code

If you wish to fork or modify the code, visit the [GitHub project page][scm], where the latest versions are always kept. Check the 'master' branch for the latest release, and the 'develop' for the current, and stable, development version.

## License
The project has been released under the [MIT License][license].

[issues]: https://github.com/Bernardo-MG/maven-github-deployment-action/issues
[license]: https://www.opensource.org/licenses/mit-license.php
[scm]: https://github.com/Bernardo-MG/maven-github-deployment-action
