pipeline{
    agent any 

    stages {
        stage('Prueba de Conexion ssh'){
            steps {
            withCredentials([sshUserPrivateKey(credentialsId: 'e0f51ef7-be00-439e-8675-3771459564ae', keyFileVariable: 'llave', passphraseVariable: '', usernameVariable: 'username')]) {
               sh """
                ssh-keyscan -H 192.168.0.20 >> ~/.ssh/known_hosts;               
                ssh $llave $username@192.168.0.20
                ls -la
                pwd
                """
                }
                
            }


        }

    }

}