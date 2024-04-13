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

```
sudo unzip apache-maven-3.8.8-bin.zip 
```

```
sudo rm -rf apache-maven-3.8.8-bin.zip
```

### Step 3: Set Environment Variable (Setting the home of Maven)

### Edit the ~/.bash_profile

```
vi ~/.bash_profile    #may need to use sudo
```

### Add the following to the ~/.bash_profile

*export M2_HOME=/opt/apache-maven-3.8.8*

*export PATH=$PATH:$M2_HOME/bin*

- Run the following to restart

```
source ~/.bash_profile
```

### Step 4: Check the Maven version installed

```
mvn -version
```


### create project directory and then navigate to project directory (location should be home/root)

```
mkdir maven-project
```

```
cd maven-project
```

### Git clone repo into project directory (from github)

```
git clone https://.....
```

### cd into the cloned repo and delete all files except 'src' and 'pom.xml'

```
cd web-app
```

### Start Maven lifecycle with the following commands

```
mvn clean
```

```
mvn package
```

```
ls          #To see our new target directory
```

```
cd target
```

## **You can do same using Ubuntu but bear in mind that the commands will change based on the fact that you will be using Ubuntu**
