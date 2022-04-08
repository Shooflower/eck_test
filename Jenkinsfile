pipeline {
    agent none 
    stages {
        stage('Example Build') {
            agent { docker 'elasticsearch:8.1.2' } 
            steps {
                echo 'Hello, ES'
                sh 'curl -XGET "localhost:9092"'
            }
        }
        stage('Finish Building') {
            steps {
                echo 'Build Complete'
            }
        }
    }
}
