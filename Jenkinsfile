node {
    stage('Curl to ES') {
        withCredentials([usernamePassword(credentialsId: 'es-creds', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) {
            steps {
                echo 'Hello, ES'
                sh "curl https://elasticsearch-cluster-elastic-system.apps.ocpjaxd003.csx.com/ --insecure -u ${USERNAME}:${PASSWORD}"
            }
        }
    }
    stage('Finish Building') {
        steps {
            echo 'Build Complete'
        }
    }
}
