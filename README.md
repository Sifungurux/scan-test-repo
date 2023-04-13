# scan-test-repo

Repo containing test setup for scanning

## Prerequsist

1. Install tekton

    ``` bash
    kubectl apply --filename https://storage.googleapis.com/tekton-releases/pipeline/latest/release.yaml
    ```

2. Install pipenv

``` bash
pip install pipenv
```

## Setting up pipfile.lock

Starts a virtual environment

``` bash
pipevn shell
```

Installs a package e.g flask

``` bash
pipenv install flask==0.12.1
```

The tekton folder contains task to scan a fs folder. In this case it is a cloned repo. It is posible to used Trivy repo scan but this is to get closer to the correct repo that the tasks and pipelines are made for.

But following command can be used to directly scan a remote repo.

``` bash
trivy repo hhtps://repo_url
´´´

