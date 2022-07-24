pipeline{
    agent any
    parameters {
        string(name:'version', defaultValue: '1.1.0', description: '')
        //boolean(name:' Docker', defaultvalue: 'true', description: '')
        choice(name:'version', choices: ['1.1.0','1.2.0','1.3.0'], description: '')
    }
    stages {
   
        stage('Build') {
            steps {
                echo "Build"
                sh 'echo "${version}"'

            }
        }
        stage('Test') {
            steps {
                echo "testing"
                
            }
        }
        stage('Deploy') {
            input {
                message "should be continue"
                ok "yes we should"
            }
            steps {
               echo "deploy to prod"
                
            }
        }

    }
    post{
        always{
            echo "i will always run"
        }
        success {
            echo "all stage success run"
        }
        failure{
            echo "failure"
        }
    }
}
