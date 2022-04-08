podTemplate(yaml: '''
    apiVersion: v1
    kind: Pod
    metadata:
      labels:
        label: elastic
    spec:
      serviceAccountName: default
      containers:
      - name: elasticsearch
        image: elasticsearch:8.1.2

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

