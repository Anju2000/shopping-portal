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
                echo 'this is the test job'
                sh 'npm test'
                sleep 3
            }
        }
        stage('package-app'){
            steps{
                echo 'this is the package job'
                sh 'npm run package'
                sleep 3
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}
