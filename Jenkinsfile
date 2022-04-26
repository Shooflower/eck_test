podTemplate(
    containers: [
        containerTemplate(
            name: 'elasticsearch', image: 'elasticsearch', command: 'sleep', args: '99d'
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