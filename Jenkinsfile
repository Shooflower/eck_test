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
                withCredentials([usernameColonPassword(credentialsId: 'es-creds-local', variable: 'USERPASS')]){
                    sh 'curl -XGET https://localhost:9200 -k -u $USERPASS'
                }
            }
        }
    }
}