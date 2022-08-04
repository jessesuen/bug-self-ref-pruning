# Self-referential Pruning Bug

This repo reproduces bug where Argo CD will prune a resource which is not self-referential and Argo CD is configured with annotation based tracking.

Steps:
1. Create an app named `self-ref-bug` with the source as the contents of `self-ref-bug` directory.
2. `kubectl create -f ./manual-apply`
3. Refresh the `self-ref-bug` application
4. Sync with prune and see the second ConfigMap get pruned.
