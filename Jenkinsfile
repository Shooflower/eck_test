podTemplate(
    containers: [
        containerTemplate(
            name: 'centos', image: 'centos', command: 'sleep', args: '99d'
        )
    ]
) {
    node(POD_LABEL){
        stage('Test Curl'){
            container('centos'){
                sh 'curl -XGET https://elasticsearch-cluster-elastic-system.apps.ocpjaxd003.csx.com/ --insecure'
            }
        }
    }
}