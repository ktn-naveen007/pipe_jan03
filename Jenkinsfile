pipeline{
agent {label 'Node_Ub'}
    stages{
        stage('initialize'){
            steps{

                 checkout scm
            }
         
        }

        stage('compile'){
            steps{

                echo 'compile phase'
          sh  '''
            mvn compile

            '''                 
            }
        }
            stage('test'){
            steps{
                echo 'test phase'
         sh   '''
            mvn test

            '''                 
            }
            }
            stage('deploy'){
                steps{
                    sh '''
                       mvn package
                       /home/yash/naveen/.f1
                    '''
                }
            }
         
        }
    }
