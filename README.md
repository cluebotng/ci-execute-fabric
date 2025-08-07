# `fabric` based GitHub action

This action provides a helper interface for running `fabric` based tasks.

Example usage:

```
  deploy:
    runs-on: ubuntu-latest
    needs: [release]
    steps:
      - uses: actions/checkout@v4
      - uses: cluebotng/ci-execute-fabric@main
        with:
          task: deploy-report
          release: ${{ github.ref }}
          ssh_key: ${{ secrets.CI_SSH_KEY }}
```
