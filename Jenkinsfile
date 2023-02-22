pipeline {
    agent any
    options{
        timestamps()
        ansiColor('xterm')
    }
    stages {
        stage('Crear entorno EB'){
            steps {
                 withAWS(credentials: 'Credentials_aws', region: 'eu-west-1') {
                    dir("proyecto") {
                        sh 'eb create mi-entorno-dev'
                    }
                 }
            }
        }
    }
}
