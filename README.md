# jxboot-resources

Helm chart for resources used by [jx boot](https://jenkins-x.io/getting-started/boot/)

See chart [readme](./jxboot-resources/README.md) for install and config options.


## Using the test harness

This is a complex helm chart which can generate lots of different output depending on the input `values.yaml` so we use the little helm test harness [jenkins-x/helm-unit-tester](https://github.com/jenkins-x/helm-unit-tester).

To try the tests:

```bash
make test
```

the exemplar data in `tests/test_data/*/expected/**/*.yaml` is dependent on the values but also some of the data depends on the underlying chart stuff. So you can regenerate the exemplar test data via:

```bash
make test-regen
```