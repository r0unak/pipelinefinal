pipeline{
        agent any
        
        stages{
            stage('SCM'){
                steps{
                    git credentialsId: 'github', url: 'https://github.com/r0unak/pipeline.git'   
                }
            }
        
            stage('NodeJSBuild'){
                steps{
                    sh "npm install"
                }
            }
            
            stage('Docker Build'){
                steps{
                    sh "docker build -t rounak87/nodet:0.0.1 ."
                }
            }
            
        }
        
        
}
