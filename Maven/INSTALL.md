# Steps to Install Maven

- We could do the installation either:
  1. Manually
  2. Run a script do the installation before deploying
 
# Installing Maven on RedHat

### Step 1:

### Navigate to the /opt directory to do the installation

```
cd /opt
```

### Download and install requirements (git & java)

```
sudo yum install wget nano tree unzip git -y
```

```
sudo yum install java-11-openjdk-devel java-1.8.0-openjdk-devel -y
```

![1_java_install.png](/Maven/Images/1_java_install.png)

### Check to confirm installation of git & java

```
java -version
```

```
git --version
```

![2_java_git_version.png](/Maven/Images/2_java_git_version.png)

### Step 2: Install Maven      (Steps from here onwards can be scripted to run so you do not have to do it manually)
### Download the Maven Software

```
sudo wget https://dlcdn.apache.org/maven/maven-3/3.8.8/binaries/apache-maven-3.8.8-bin.zip
```

![3_maven_download.png](/Maven/Images/3_maven_download.png)

```
sudo unzip apache-maven-3.8.8-bin.zip 
```

![4_maven_unzip.png](/Maven/Images/4_maven_unzip.png)

```
sudo rm -rf apache-maven-3.8.8-bin.zip
```

![5_re_maven_download.png](/Maven/Images/5_re_maven_download.png)


### Step 3: Set Environment Variable (Setting the home of Maven)

### Edit the ~/.bash_profile

```
vi ~/.bash_profile    #may need to use sudo
```

### Add the following to the ~/.bash_profile

*export M2_HOME=/opt/apache-maven-3.8.8*

*export PATH=$PATH:$M2_HOME/bin*

![6_bash_profile.png](/Maven/Images/6_bash_profile.png)

- Run the following to restart

```
source ~/.bash_profile
```

### Step 4: Check the Maven version installed

```
mvn -version
```

![7_mvn_version.png](/Maven/Images/7_mvn_version.png)

### create project directory and then navigate to project directory (location should be home/root)

```
mkdir maven-project
```

```
cd maven-project
```

![8_project_dir.png](/Maven/Images/8_project_dir.png)

### Git clone repo into project directory (from github)

```
git clone https://.....
```

![9_git_clone.png](/Maven/Images/9_git_clone.png)

### cd into the cloned repo and delete all files except 'src' and 'pom.xml'

```
cd web-app
```

![10_cd_project_dir.png](/Maven/Images/10_cd_project_dir.png)

![11_delete_files.png](/Maven/Images/11_delete_files.png)

### Start Maven lifecycle with the following commands

```
mvn clean
```

![12_mvn_clean1.png](/Maven/Images/12_mvn_clean1.png)

![13_mvn_clean2.png](/Maven/Images/13_mvn_clean2.png)

```
mvn package
```

![14_mvn_package1.png](/Maven/Images/14_mvn_package1.png)

![15_mvn_package2.png](/Maven/Images/15_mvn_package2.png)

```
ls          #To see our new target directory
```

```
cd target
```

![16_target_dir.png](/Maven/Images/16_target_dir.png)

## **You can do same using Ubuntu but bear in mind that the commands will change based on the fact that you will be using Ubuntu**
