### 이미지 교체
```
kubectl set image deployment/toc-ai-fe-deployment \
  ksox-ai-fe=<이미지 registry 주소>/<repo>:<tag> \
  -n toc
```
