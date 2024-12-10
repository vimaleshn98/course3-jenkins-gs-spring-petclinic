pipeline{
    agent{
         label 'agent1'
    }
    parameters{
                    string(name: "name", defaultValue: "vimalesh")
                } 
    stages{
        stage('Build'){
            steps{
                echo(message: 'build')
                echo(message: '${env.BUILD_ID} ${param.name}')                
            }            
        }
        stage('Test'){
            steps{
                echo(message: 'Test')
                echo(message: '${env.BUILD_ID}')                
            }            
        }
        stage('Publish'){
                 
            steps{
                echo(message: 'Publish')
                echo(message: '${env.BUILD_ID}')
                sh(script: 'hostname')
                            
            }            
        }
    }
}