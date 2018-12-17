pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                sh ' echo $pwd ' 
                sh 'echo " Etape 0- Clonnage depo Git" '
                sh ' rm -f resultat* RESULTAT* '
               // sh 'git clone https://github.com/ilefnlebhar/DepotScript.git workstation1'
                sh '''
                    chmod 755 ./*.sh
                '''
            }
        }        
        stage('Build') {
            steps {
                sh 'echo "Etape-1 Build " '
                sh '''
                 
                  ./script1.sh
                '''
            }
        }

        
        stage('Deploy') {
            steps {
                sh 'echo "Etape-2 Deploy" '
                sh ''' 
                  ./script2.sh
                '''
            }
        }  
        stage('Test') {
            steps {
                sh 'echo "Etape-3 : Test " '
                sh '''
                    
                    ./script3.sh 
                '''
            }
        }  
        
    }
}

