# kubeflow-demo


px-deploy create -n px1 -t px</br>
</br>
yum install wget -y</br>
kubectl patch storageclass px-csi-db -p '{"metadata": {"annotations":{"storageclass.kubernetes.io/is-default-class":"true"}}}'</br>
</br>
CPU-only</br>
curl -sfL https://get.k3ai.in | bash -s -- --cpu --plugin_kfpipelines</br>
GPU support</br>
</br>
# env/platform-agnostic-pns hasn't been publically released, so you will install it from master</br>
export PIPELINE_VERSION=2.0.0</br>
kubectl apply -k "github.com/kubeflow/pipelines/manifests/kustomize/cluster-scoped-resources?ref=2.0.0"</br>
kubectl wait --for condition=established --timeout=60s crd/applications.app.k8s.io</br>
kubectl apply -k "github.com/kubeflow/pipelines/manifests/kustomize/env/platform-agnostic-pns?ref=2.0.0"</br>
</br>
load generator</br>
python3 -m pip install https://storage.googleapis.com/ml-pipeline/release/0.1.10/kfp.tar.gz --upgrade</br>
</br>

