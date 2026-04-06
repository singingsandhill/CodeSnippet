### 이미지 교체
```
kubectl set image deployment/toc-ai-fe-deployment \
  ksox-ai-fe=<이미지 registry 주소>/<repo>:<tag> \
  -n toc
```

### Secret 수정
```
kubectl edit secret toc-ai-be-secret -n toc
```

### 수정 후 재배포
```
kubectl rollout restart deployment dev-toc-fe-deployment -n dev-toc
```

### 이벤트 확인
```
kubectl get events -n toc --sort-by=.metadata.creationTimestamp
```
