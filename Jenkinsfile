podTemplate(
    containers: [
        containerTemplate(
            name: 'elasticsearch', 
            image: 'elasticsearch:8.1.3', 
            command: 'sleep', 
            args: '99d',
            ports: [
                '9200'
            ]
        )
    ]
) {
    node(POD_LABEL){
        stage('Test Curl'){
            container('elasticsearch'){
                sh 'curl -XGET http://localhost:9200'
            }
        }
    }
}