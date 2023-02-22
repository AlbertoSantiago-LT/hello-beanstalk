pipeline {
    agent any
    options{
        timestamps()
        ansiColor('xterm')
    }
    stages {
        stage('Crear entorno EB B'){
            steps {
                 withAWS(credentials: 'Credentials_aws', region: 'eu-west-1') {
                    dir("app") {
                        sh 'eb create entorno-dev-eb'
                    }
                 }
            }
        }
    }
}
