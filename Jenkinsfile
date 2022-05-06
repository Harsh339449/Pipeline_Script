pipeline {
    agent any
    stages {
        stage('Non Prarllel Stage') {
            agent{
                label 'built-in'
            }
            steps {
                echo 'Compiled Successfully!!'
            }
        }
        
        
         stage('Run Tests') {
             parallel{
                 stage('Test on Master'){
                     agent{
                         label 'built-in'
                     }
                     steps {
                      echo 'Task to master!!'
                     }
                 }
                  stage('Test on Slave'){
                     agent{
                         label 'Slave_Agent_1'
                     }
                     steps {
                      echo 'Task to Slave!!'
                     }
                 }
             }
            
        }
    }

}
