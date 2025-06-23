pipeline {
    agent any

    stages {
        stage('Run Selected Action') {
            steps {
                script {
                    def choice = sh(script: "python3 main.py", returnStdout: true).trim()
                    echo "🔀 Selected Action: ${choice}"

                    if (choice == "1") {
                        sh "python3 action1.py"
                    } else if (choice == "2") {
                        sh "python3 action2.py"
                    } else if (choice == "3") {
                        sh "python3 action3.py"
                    } else {
                        error "Invalid action choice: ${choice}"
                    }
                }
            }
        }
    }
}
