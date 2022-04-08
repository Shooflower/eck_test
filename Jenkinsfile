node {
    stage('Curl to ES') {
        withCredentials([usernameColonPassword(credentialsId: 'es-creds', variable: 'AUTHORIZATION')]){
            steps {
                echo 'Hello, ES'
                sh 'curl https://elasticsearch-cluster-elastic-system.apps.ocpjaxd003.csx.com/ --insecure -H "Authorization: Basic amVua2luczpwYXNzdzByZA=="'
            }
        }
    }
    stage('Finish Building') {
        steps {
            echo 'Build Complete'
        }
    }
}
