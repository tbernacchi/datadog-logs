<h1 align="">Datadog logs 👋</h1>
<p>
</p>

> Send logs from k8s cluster to datadog.

![Datadog](/.github/assets/img/datadog-logo.png)

<div align=>
	<img align="center" width="400px" src=/.github/assets/img/gke-logo.png>
</div>

## Table of Contents

* **GKE**  
  * [Official Website](https://cloud.google.com/kubernetes-engine)
  * [Official Docs](https://cloud.google.com/kubernetes-engine/docs/quickstart)
  * [Official Github](https://github.com/GoogleCloudPlatform/kubernetes-engine-samples)

* **Datadog**  
  * [Official Website](https://www.datadoghq.com/)
  * [Official Docs](https://docs.datadoghq.com/)
  * [Official Github](https://github.com/DataDog)

## Requirements
* Google Cloud SDK + gcloud CLI + kubectl + helm;
* Datadog account + Apikey;

## Usage

```
gcloud auth login
gcloud components update
gcloud config set project <my-project>
gcloud container clusters create my-cluster-datadog --zone southamerica-east1-a --project <my-project>
```

```
helm repo add datadog https://helm.datadoghq.com
helm repo add stable https://charts.helm.sh/stable
helm repo update
kubectl create namespace datadog
```

```
helm install tadeu-teste-datadog -f values.yml -n datadog --set datadog.site='datadoghq.com' --set datadog.apiKey=myapikeyec747bdd2b92a3fc42345678 datadog/datadog
```

## Author

👤 **Tadeu Bernacchi**

* Website: http://www.tadeubernacchi.com.br/
* Twitter: [@tadeuuuuu](https://twitter.com/tadeuuuuu)
* Github: [@tbernacchi](https://github.com/tbernacchi)
* LinkedIn: [@tadeubernacchi](https://linkedin.com/in/tadeubernacchi)

## Show your support

Give a ⭐️ if this project helped you!

***
_This README was generated with ❤️ by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_
