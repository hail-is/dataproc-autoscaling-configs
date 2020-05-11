# dataproc-autoscaling-configs


Create policies max-10, max-50, max-100, max-500:
```
for POLICY in "max-10" "max-50" "max-100" "max-500"; do
    gcloud dataproc autoscaling-policies import ${POLICY} --source \
      <(curl https://raw.githubusercontent.com/hail-is/dataproc-autoscaling-configs/master/${POLICY}-preemptibles.yaml)
done
```
