### Azure VM 접속
```
az network bastion ssh --name ${BASTION_NAME} --resource-group ${BASTION_RESOURCE_GROUP_NAME} --target-resource-id ${TARGET_VM_ID} --auth-type AAD
```
