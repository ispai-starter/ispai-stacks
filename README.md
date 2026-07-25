# ispai-stacks — GitOps stacks do ISP-AI

**Artefato gerado — NÃO edite à mão.** Fonte da verdade: `ispai-starter/ispai-installer/stacks/04..09`.
`ispai.yaml` é produzido por `installer/merge-stacks.py` (combina redis/postgres/minio/n8n/waha/chatwoot
num único compose `ispai`, serviços `ispai_<svc>`; força `replicas:0` em n8n webhook/worker — B1/[ADR-0015]).

O Portainer consome este repo via `POST /api/stacks/create/swarm/repository` (`type=repository`,
`ComposeFile=ispai.yaml`). Ver `ispai-installer/docs/specs/data/gitops-stacks-repo.md`.

Regenerar: `python3 installer/merge-stacks.py stacks/ > ispai.yaml`
