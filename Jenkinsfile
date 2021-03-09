def remote = [:]
remote.name = "node"
remote.host = "104.43.194.198"
remote.allowAnyHosts = true

node {
    withCredentials([usernamePassword(credentialsId: 'a72759b4-2f4f-4545-b1f7-db1fa4e6f977', passwordVariable: 'password', usernameVariable: 'userName')]) {
        remote.user = userName
        remote.password = password

        stage("SSH Steps Rocks!") {
            sshCommand remote: remote, command: "ls /home/devops/"
            sshPut remote: remote, from: 'C:\\Users\\svaichalkar\\.jenkins\\workspace\\BTS_MavenSelenium_POC_v1.0\\target\\poc-devopsDemo.jar', into: '/home/devops/poc'
        }
    }

}
