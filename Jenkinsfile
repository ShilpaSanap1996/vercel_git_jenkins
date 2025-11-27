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
                bat 'npx vercel-token deploy --prod --token=I0UZD6wNfcrmw7WEzEMqlYU8 --yes'
            }
        }
    }
}