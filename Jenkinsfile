pipeline{
agent {label 'Node_ub'}
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

            stage('test'){
            steps{
                echo 'test phase'
         sh   '''
            mvn test

            '''                 
            }
         
        }
    }
}