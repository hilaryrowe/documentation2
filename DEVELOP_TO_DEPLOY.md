## Developing + building + deploying the "Documentation" GitBook repository
See [README.md](README.md) for more information on what Documentation is used for.

### Developing
To develop our Gitbook we're using docker.  Docker will run the 'gitbook serve' command on port 4000 on your local host.  It will also mount the documentation repository at ~/code/documentation.  Any time a file changes in ~/code/documentation, gitbook will reload the server and your changes will be rendered.

0. [Install Docker](URL TO CONFLUENCE)
0. cd ~/code/documentation

#### Run in foreground
0. cd ~/code/documentation
0. docker-compose up
  - Use Ctrl + C to stop

#### Run in background
0. cd ~/code/documentation
0. docker-compose up -d
0. docker-compose stop

### Building (Meant to be run by Jenkins)
0. cd ~/code/documentation
0. script/build.sh
0. a ```_book``` directory will be generated in ~/code/documentation

### Installing Gitbook Plugins
0. cd ~/code/documentation
0. Stop existing docker-compose up instance
0. Edit book.json and add to plugins section (http://toolchain.gitbook.com/plugins/)
0. docker-compose run --rm gitbook gitbook install
0. docker-compose up
0. If things work.... (assuming you're on latest master) 
  0. git checkout -b master_add_plugin_x
  0. git add node_modules book.json
  0. git commit -m "Adding plugin x"
  0. git push origin master_add_plugin_x
  0. Open pull request on branch, Tag someone from Devops or just merge that bugger

### Deploying

```
Note this process will likely change in the future to support promotion or pipelines
```

0. Commit your changes to master
0. Navigate to [Jenkins](http://jenkins.int.sightmachine.com/view/Documentation/)
0. Run the [Build Job](http://jenkins.int.sightmachine.com/view/Documentation/job/sightmachine-documentation-build/)
   0. The deploy targets will use the last successful artifact
0. Choose your deploy target
   - [stage2](http://jenkins.int.sightmachine.com/view/Documentation/job/sightmachine-documentation-deploy-to-stage2/)
   - [stage3](http://jenkins.int.sightmachine.com/view/Documentation/job/sightmachine-documentation-deploy-to-stage3/)
   - [stage4](http://jenkins.int.sightmachine.com/view/Documentation/job/sightmachine-documentation-deploy-to-stage4/)
   - [stage5](http://jenkins.int.sightmachine.com/view/Documentation/job/sightmachine-documentation-deploy-to-stage5/)
   - [stage6](http://jenkins.int.sightmachine.com/view/Documentation/job/sightmachine-documentation-deploy-to-stage6/)
   - [production](http://jenkins.int.sightmachine.com/view/Documentation/job/sightmachine-documentation-deploy-to-production/)

### Support/Troubleshooting

Please Join #devops in Slack!

