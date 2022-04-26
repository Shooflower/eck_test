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
                withEnv(['HTTP_PROXY=http://webproxy.csx.com:8080', 'HTTPS_PROXY=http://webproxy.csx.com:8080']){
                    withCredentials([usernameColonPassword(credentialsId: 'es-creds', variable: 'USERPASS')]){
                        sh 'curl -XGET https://elasticsearch-cluster-elastic-system.apps.ocpjaxd003.csx.com/ -k -u $USERPASS'
                    }
                }
            }
        }
    }
}