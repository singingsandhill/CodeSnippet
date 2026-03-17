### Pod 목록 조회
```
kubectl get pods -o wide -n toc
```

### 특정 pod 로그 조회
```
kubectl logs -n toc toc-ai-be-deployment-74ff9cb56c-mv96k
```

### ConfigMap 조회
```
kubectl get configmap -n toc
```
