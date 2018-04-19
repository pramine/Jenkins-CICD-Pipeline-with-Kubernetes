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
        stage('Docker Container') {
            container('docker'){
                sh "docker info"
                sh "docker pull ubuntu"
                sh "sleep 60"
            }
        }
        stage('Helm') {
            container('helm'){
                sh "helm ls"
                sh "helm status jenkins"
            }
        }      
        stage('KubeCtl') {
            container('kubectl'){
                sh "kubectl version"
            }
        } 
    }
}
