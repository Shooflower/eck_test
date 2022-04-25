pipeline {
    agent any
    environment {
        ES_CREDS = credentials('es-creds')
    }
    stages {
        stage('Test ES GET') {
            steps {
                sh('/usr/bin/curl -u $ES_CREDS_USR:$ES_CREDS_PSW https://elasticsearch-cluster-elastic-system.apps.ocpjaxd003.csx.com/ --insecure')
            }
        }
        stage("Build Complete"){
            steps {
                sh('echo COMPLETED BUILD!')
            }
        }
    }
}
