# kubectl context notes

Quick notes for switching contexts when poking around clusters.

## Current context

```bash
kubectl config current-context
```

## List contexts

```bash
kubectl config get-contexts
```

## Switch context

```bash
kubectl config use-context <name>
```

## Save a context

```bash
kubectl config set-context <name> --cluster=<cluster> --user=<user> --namespace=<ns>
```

## Useful alias

```bash
alias kc='kubectl config use-context'
```

Remember to update `KUBECONFIG` if you are juggling multiple files:
`KUBECONFIG=~/.kube/config:~/work/config kubectl config view --merge`
