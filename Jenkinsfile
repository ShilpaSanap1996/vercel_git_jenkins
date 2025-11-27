pipeline{
    agent any

    environment {
        VERCEL_TOKEN =credentials('vercel-token')
    }
    stages{
        stage('Install'){
            steps{
                bat 'npm install'
            }
        }
        stage('test'){
            steps{
                echo 'testing ....'
            }
        }
        stage('build'){
            steps{
                bat 'npm run build'
            }
        }
        stage('deploy'){
            steps{
                bat 'npx vercel --prod --token=u0CNsTZYDheRUiKh0mKtGbGQ --yes'

            }
        }
    }
}