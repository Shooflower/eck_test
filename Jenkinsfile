podTemplate(
    label: 'myPod',
    containers: [
        containerTemplate(
            name: 'centos', image: 'centos', command: 'cat'
        )
    ]
) {
    node('myPod'){
        stage('Test Curl'){
            container('centos'){
                sh 'curl -XGET https://elasticsearch-cluster-elastic-system.apps.ocpjaxd003.csx.com/ --insecure'
            }
        }
    }
}
