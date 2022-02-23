pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       nodejs 'nodejs' 
    }
    

    stages{
        stage('compile-app'){
            steps{
                echo 'this is the compile job'
                sh 'npm install'
            }
        }
        stage('test-app'){
            steps{
                echo 'this is the second job'
                sh 'npm test'
            }
        }
        stage('package-app'){
            steps{
                echo 'this is the third job'
                sh 'npm run package'
            }
        }
    }
    
    post{
        always{
            echo 'Hey I know how to create pipeline as code...'
        }
        
    }
    
}
