pipeline{
    agent any 

    stages {
        stage('Prueba de Conexion ssh'){
            steps {
                sh """
                ssh -i pruebas docker@192.168.0.20
                ls -la
                """
            }


        }

    }

}