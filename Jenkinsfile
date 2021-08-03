
/*def remote = [:]
remote.name = "docker"
remote.host = "192.168.0.20"
remote.allowAnyHosts = true
*/
pipeline{
    agent any 

    stages {
        stage('Prueba de Conexion ssh'){
            steps {
                /*sshagent(credentials:['UserandPassword']){
                    sh 'pwd'*/
                def remote = [:]
                   remote.name = 'birc'
                   remote.host = "190.85.106.202"
                   remote.port = 2224
                   remote.allowAnyHosts = true
                withCredentials([usernamePassword(credentialsId: 'UserandPassword', passwordVariable: 'password', usernameVariable: 'username')]) {
                // some block
                remote.user = username
                remote.password = password
                sshCommand remote: remote, command: 'ls -la'
                }
                }
                
                
                
                
                
                
                /*
            withCredentials([sshUserPrivateKey(credentialsId: 'e0f51ef7-be00-439e-8675-3771459564ae', keyFileVariable: 'llave', passphraseVariable: '', usernameVariable: 'username')]) {
               sh """
                ssh-keyscan -H 192.168.0.20 >> ~/.ssh/known_hosts;               
                ssh $llave $username@192.168.0.20
                ls -la
                pwd
                """
                withCredentials([usernamePassword(credentialsId: 'UserandPassword', passwordVariable: 'SERVER_PASSWORD', usernameVariable: 'SERVER_USER')]) {
                
                remote.user= SERVER_USER;
                remote.password= SERVER_PASSWORD;

                sshCommand remote: remote, command: 'ls -la'
                */
            
                    }
                }
                
            }
        }
    

