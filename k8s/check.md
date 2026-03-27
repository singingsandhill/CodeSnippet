### Pod 목록 조회
```
kubectl get pods -o wide -n toc
```

### 특정 pod 로그 조회
```
kubectl logs -n toc toc-ai-be-deployment-74ff9cb56c-mv96k
```
```
kubectl describe pod -n toc toc-ai-fe-deployment-675465976b-b5q89
```
### 환경변수 관련
#### ConfigMap 조회
```
kubectl get configmap -n toc
```
#### secret 조회
```
kubectl get secret -n toc
```

### 설정 수정
```
kubectl edit configmap toc-ai-be-configmap -n toc
```
