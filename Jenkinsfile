pipeline {
    agent none
    stages {
        stage ('Latest SWP') {
            agent { 
                label 'local'
            }
            steps {
                script {
                    sh ''' #!/bin/bash
                    ls -Art ../../swp/*.swp | tail -n 1 | awk -F "-" '{print substr($4, 1, length($4)-4)}'
                    '''
                    }
            }
        }
    }
}
