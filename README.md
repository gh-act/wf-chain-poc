# wf-chain-poc

Does a `workflow_run` chain hanging off `pull_request_target` fire at every level on a public repo, for fork PRs, same-repo PRs and pushes?

`Request` (pull_request_target, push) → `L1` → `L2` → `L3` → `L4`, each `workflow_run: completed` on the previous one. Each job writes its trigger context to the step summary.

Context: envoyproxy/envoy-ci-staging#2169.
same-repo PR
