### argocd tls
出现多次 too many redirects 的问题在于： https://github.com/argoproj/argo-cd/issues/2953
需要 --insecure， 采用 insecure 方式。