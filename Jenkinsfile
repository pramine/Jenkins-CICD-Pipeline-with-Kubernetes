podTemplate(label: 'mypod', serviceAccount: 'jenkins', containers: [
    containerTemplate(name: 'docker', image: 'docker', ttyEnabled: true, command: 'cat'),
    containerTemplate(name: 'kubectl', image: 'lachlanevenson/k8s-kubectl:v1.8.0', command: 'cat', ttyEnabled: true),
    containerTemplate(name: 'helm', image: 'lachlanevenson/k8s-helm:latest', command: 'cat', ttyEnabled: true)
  ],
  volumes: [
    hostPathVolume(mountPath: '/var/run/docker.sock', hostPath: '/var/run/docker.sock'),
  ]) {

    node('mypod') {
        ////////// Step 1 //////////
        stage('Git Clone And Setup') {
            container('docker'){
                sh "docker info"
                sh "docker pull ubuntu"
            }
            container('helm'){
                sh "helm ls"
                sh "helm status jenkins"
            }
            container('kubectl'){
                sh "kubectl version"
                sh "kubectl get all --all-namespaces"
            }
        }
        stage('Build & Unit Test') {
            container('docker'){
                sh "docker info"
                sh "docker pull ubuntu"
            }
            container('helm'){
                sh "helm ls"
                sh "helm status jenkins"
            }
            container('kubectl'){
                sh "kubectl version"
                sh "kubectl get all --all-namespaces"
            }
        }
        stage('Functional Tests') {
            container('docker'){
                sh "docker info"
                sh "docker pull ubuntu"
            }
            container('helm'){
                sh "helm ls"
                sh "helm status jenkins"
            }
            container('kubectl'){
                sh "kubectl version"
                sh "kubectl get all --all-namespaces"
            }
        }
        stage('Publish Docker Image and Helm Charts') {
            container('docker'){
                sh "docker info"
                sh "docker pull ubuntu"
            }
            container('helm'){
                sh "helm ls"
                sh "helm status jenkins"
            }
            container('kubectl'){
                sh "kubectl version"
                sh "kubectl get all --all-namespaces"
            }
        }
        stage('Deploy to Dev Test Environment') {
            container('docker'){
                sh "docker info"
                sh "docker pull ubuntu"
            }
            container('helm'){
                sh "helm ls"
                sh "helm status jenkins"
            }
            container('kubectl'){
                sh "kubectl version"
                sh "kubectl get all --all-namespaces"
            }
        }
        stage('Dev Tests') {
            container('docker'){
                sh "docker info"
                sh "docker pull ubuntu"
            }
            container('helm'){
                sh "helm ls"
                sh "helm status jenkins"
            }
            container('kubectl'){
                sh "kubectl version"
                sh "kubectl get all --all-namespaces"
            }
        }
        stage('Cleanup Dev Test Environment Deployment') {
            container('docker'){
                sh "docker info"
                sh "docker pull ubuntu"
            }
            container('helm'){
                sh "helm ls"
                sh "helm status jenkins"
            }
            container('kubectl'){
                sh "kubectl version"
                sh "kubectl get all --all-namespaces"
            }
        }
        stage('Go for Staging Environment Deployment?') {
            container('docker'){
                sh "docker info"
                sh "docker pull ubuntu"
            }
            container('helm'){
                sh "helm ls"
                sh "helm status jenkins"
            }
            container('kubectl'){
                sh "kubectl version"
                sh "kubectl get all --all-namespaces"
            }
        }
        stage('Deploy to Staging Environment') {
            container('docker'){
                sh "docker info"
                sh "docker pull ubuntu"
            }
            container('helm'){
                sh "helm ls"
                sh "helm status jenkins"
            }
            container('kubectl'){
                sh "kubectl version"
                sh "kubectl get all --all-namespaces"
            }
        }
        stage('Staging Tests') {
            container('docker'){
                sh "docker info"
                sh "docker pull ubuntu"
            }
            container('helm'){
                sh "helm ls"
                sh "helm status jenkins"
            }
            container('kubectl'){
                sh "kubectl version"
                sh "kubectl get all --all-namespaces"
            }
        }
        stage('Cleanup Staging Environment Deployment') {
            container('docker'){
                sh "docker info"
                sh "docker pull ubuntu"
            }
            container('helm'){
                sh "helm ls"
                sh "helm status jenkins"
            }
            container('kubectl'){
                sh "kubectl version"
                sh "kubectl get all --all-namespaces"
            }
        }
        stage('Go for Production Environment Deployment?') {
            container('docker'){
                sh "docker info"
                sh "docker pull ubuntu"
            }
            container('helm'){
                sh "helm ls"
                sh "helm status jenkins"
            }
            container('kubectl'){
                sh "kubectl version"
                sh "kubectl get all --all-namespaces"
            }
        }
        stage('Deploy to Production Environment') {
            container('docker'){
                sh "docker info"
                sh "docker pull ubuntu"
            }
            container('helm'){
                sh "helm ls"
                sh "helm status jenkins"
            }
            container('kubectl'){
                sh "kubectl version"
                sh "kubectl get all --all-namespaces"
            }
        }
        stage('Production Tests') {
            container('docker'){
                sh "docker info"
                sh "docker pull ubuntu"
            }
            container('helm'){
                sh "helm ls"
                sh "helm status jenkins"
            }
            container('kubectl'){
                sh "kubectl version"
                sh "kubectl get all --all-namespaces"
		sh "End of Pipelin"
            }
        }
    }
}
