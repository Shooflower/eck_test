podTemplate(yaml: '''
    apiVersion: v1
    kind: Pod
    metadata:
      labels:
        label: elastic
    spec:
      serviceAccountName: jenkins
      containers:
      - name: elasticsearch
        image: docker.artifactory.csx.com/elasticsearch:6.4.3

'''){
    node (POD_LABEL) {

        stage("Checkout Source"){
            checkout scm
        }

        stage ('Build') {
            sh 'echo Creating ES container'
            container(elasticsearch){
                sh 'pwd'
            }
        }
    }
}
