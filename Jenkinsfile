pipeline{
    agent any 

    stages {
        stage('Prueba de Conexion ssh'){
            steps {
                sh """
                ssh-keyscan -H 192.168.0.20 >> ~/.ssh/known_hosts;
                chmod 400 pruebas
                ssh -i pruebas docker@192.168.0.20

                ls -la
                """
            }


        }

    }

}