# Matrix use case — task resource

See [`cml.yml`](https://github.com/0x2b3bfa0/cml-use-case-matrix-task/blob/702570f99addc75a56267899f3bcead92d02061a/.github/workflows/cml.yml) and [`tpi.tf`](https://github.com/0x2b3bfa0/cml-use-case-matrix-task/blob/702570f99addc75a56267899f3bcead92d02061a/tpi.tf) for more information.

## Secrets

### GitHub

- [`REPO_TOKEN` — personal access token](https://cml.dev/doc/self-hosted-runners?tab=GitHub#pat)

### Amazon Web Services

- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`
- `AWS_SESSION_TOKEN` (optional)

See [the documentation](https://cml.dev/doc/self-hosted-runners?tab=AWS#cloud-compute-resource-credentials) for more information.

##  Matrix

- [`TF_VAR_parallelism` — how many self–hosted runners to launch](https://github.com/0x2b3bfa0/cml-use-case-matrix-task/blob/702570f99addc75a56267899f3bcead92d02061a/.github/workflows/cml.yml#L7)
- [`matrix` — what to run on the self–hosted runners](https://github.com/0x2b3bfa0/cml-use-case-matrix-task/blob/702570f99addc75a56267899f3bcead92d02061a/.github/workflows/cml.yml#L41)

Note that `parallelism` should be the n–ary cartesian product of the `matrix` choices in order to run all of them in parallel.
