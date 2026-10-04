# platform

플랫폼 컴포넌트의 GitOps 데이터입니다. 사람이 고치지 않습니다.

| 경로 | 쓰는 쪽 | 읽는 쪽 |
|---|---|---|
| `aws-dev-management/<repo>.yaml` | 각 서비스 레포의 Deploy platform 워크플로(이미지 digest) | Argo Application `iris-platform` |
| `onprem-servers/<serverKey>/values.yaml` | Deploy Worker(사용자 온프레미스 서버 등록) | ApplicationSet `iris-onprem-servers` |

push 는 GitHub webhook 으로 Argo CD 에 바로 전달됩니다(iris-infra `docs/runbooks/argocd-webhook.md`).
