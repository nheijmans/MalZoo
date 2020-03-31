![Logo](https://cloud.githubusercontent.com/assets/7534191/22924310/eb6d8948-f2a4-11e6-98f6-61125f34f075.png)
# What is MalZoo?
MalZoo is a mass static malware analysis tool that collects the information in a Mongo database
and moves the malware samples to a repository directory based on the first 4 chars of the MD5 hash.
It was build as a internship project to analyze sample sets of 50 G.B.+ (e.g. from http://virusshare.com).

A few examples where it can be used for:
- Use the collected information to visualize the results (e.g. see most used compile languages, packers etc.)
- Gather intell of large open source malware repositories (original intend of the project)
- Monitor a mailbox, analyze the emails and attachments

### Installation information on VM's and bare-metal
For more information on installation and collection of data, check out the [Wiki](https://github.com/nheijmans/malzoo/wiki/Welcome-to-the-MalZoo-wiki!) of this repository. 

### Cloud Serverless deployment
For the deployment in the AWS Cloud with a Serverless architecture, check out the repository [Malzoo Serverless](https://github.com/nheijmans/malzoo_serverless) for an auto-deployment solution.

### Docker container deployment
If you would like to deploy the Malzoo project in a Docker container, you can start very easily with pulling the image from Docker Hub 
```docker pull statixs/malzoo```

And then start a container from there. See the repository [Malzoo Container](https://github.com/nheijmans/malzoo_container) for details. 

## Information collected
See the wiki page [Information collected](https://github.com/nheijmans/MalZoo/wiki/Collected-data) which data is collected for which sample.

# Installation
See the wiki page [Installation](https://github.com/nheijmans/MalZoo/wiki/Installation-and-configuration) to see how to install MalZoo. The best option is to use the auto installation script bootstrap.sh and once that is done running you only have to execute ```export LD_LIBRARY_PATH=/usr/local/lib:$LD_LIBRARY_PATH```

# Configuration
After the installation you need to adjust the configuration file malzoo.conf in the config directory. If you are using the Splunk functionality, create a HTTP event collector token in your Splunk instance and copy the token to the configuration file (behind the Splunk part, so you replace the xxx-'es). 

# Usage
See this [Wiki page](https://github.com/nheijmans/MalZoo/wiki/Installation-and-configuration#usage) on how to use Malzoo

# Currently being developed
- AWS CloudFormation script to deploy Malzoo in AWS
- Make parts serverless for Cloud computing
- Create new modules for threat intelligence context
- Bug fixes

# Credit
Special thanks goes to the Viper project (http://viper.li). I learned alot about how to automate malware analyse by this project.
Also a big thanks to all the developers of the modules and software used and making it available for everyone to use.

# License
This project is released under the GPL 2.0 License. See the LICENSE for details.
