pipeline 
{
    agent any
    tools{
        maven "MAVEN_HOME"
    }

    stages 
    {
        stage('Build and Test') 
        {
            steps 
            {
                echo 'Build App'
                git 'https://github.com/mohitsankhla/Jenkins2.git'
                echo 'This is stage for building the project'
                bat 'mvn -Dmaven.test.failure.ignore=true clean package'
            }
        
            post {
                success {
                    junit '**/target/surefire-reports/TEST-*.xml'
                    archiveArtifacts 'target/*.jar'
                }
            }
        }
    }
}
