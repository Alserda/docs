#Capistrano


***


##### Error


 	INFO [3470de39] Running bundle exec rake db:migrate on 	178.62.204.157
	cap aborted!
	SSHKit::Command::Failed: rake stdout: Nothing written
	rake stderr: Nothing written

	Tasks: TOP => deploy:migrate
	(See full trace by running task with --trace)
	The deploy has failed with an error: #<SSHKit::Command::Failed: 	rake stdout: Nothing written
	rake stderr: Nothing written
	>

##### Oplossing

	ssh [server]
	cd railsapps/api/staging/current
	sudo service nginx stop
	bin/rake db:drop RAILS_ENV=staging
	bin/rake db:create RAILS_ENV=staging
	sudo service nginx start
	
	exit
	
	cap [staging] deploy