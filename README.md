# OpenShift Jekyll Cartridge

Pretty much everything seems to be working fine, but it can still use some testing.  

If you find any issues, please log them in the [issues](https://github.com/openshift-cartridges/openshift-jekyll-cartridge/issues) section of the [github](https://github.com/openshift-cartridges/openshift-jekyll-cartridge) project.  

###How to use this cartridge

1.)  Create a new application on OpenShift using this command:  

    rhc app create jekyll https://raw.github.com/openshift-cartridges/openshift-jekyll-cartridge/master/metadata/manifest.yml  
    
2.)  Git clone the repository that is associated with your OpenShift gear to your local machine  (the create command should do this for you)  
3.)  Change directory (cd) into the cloned repository and run the following commands (you can also use bundle install to install the gems from the Gemfile)

    gem install json jekyll

4.)  Run the following command to run the Jekyll server in watch mode (updates your changes automatically) (if you are using bundler, run "bundle exec jekyll server --watch")

    jekyll serve --watch

5.)  Make changes and updates for your site  
6.)  git add new files, git commit, and git push  
7.)  Your OpenShift gear will take care of compiling your changes and building your site!


You do not need to upload your _site folder that is created by running jekyll serve locally, as it will be generated on the server.  
It is also in the .gitignore so that you won't accidently add it :)


It will take a few minutes to install all of the gems when the gear is initially created, so be patient, it will be faster when you do a git push.

P.S. This installation also supports pygments  




