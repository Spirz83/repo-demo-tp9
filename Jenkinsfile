pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Etape de compilation...'
                sh 'chmod +x hello.sh'
                sh 'cat hello.sh'
            }
        }

        stage('Test') {
            steps {
                echo '-------------phase de tests-------------'
                sh '''
                if [ -e hello.sh ] ; then
                    echo "ok le fichier existe"
                else
                    echo "test is not ok"
                fi
                '''
                echo '-------------FIN des tests-------------'
            }
        }

        stage('Run') {
            steps {
                echo '------------DEBUT Run step-----------------'
                sh './hello.sh'
                echo '------------FIN Run step-----------------'
            }
        }
    }
}
