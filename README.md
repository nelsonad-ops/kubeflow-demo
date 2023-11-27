# kubeflow-demo


px-deploy create -n px1 -t px</br>
</br>
curl -s "https://raw.githubusercontent.com/kubernetes-sigs/kustomize/master/hack/install_kustomize.sh"  | bash</br>
ln /root/kustomize /usr/sbin/kustomize</br>
yum install wget -y</br>
kubectl apply -f kubeflow-sc.yaml
kubectl patch storageclass kubeflow-storage -p '{"metadata": {"annotations":{"storageclass.kubernetes.io/is-default-class":"true"}}}'</br>
git clone https://github.com/kubeflow/manifests.git</br>
cd manifests</br>
Single command install:</br>
while ! kustomize build example | kubectl apply -f -; do echo "Retrying to apply resources"; sleep 10; done</br>


ARCHIVE-ONLY
yum install wget -y</br>
kubectl patch storageclass kubeflow-storage -p '{"metadata": {"annotations":{"storageclass.kubernetes.io/is-default-class":"true"}}}'</br>
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

