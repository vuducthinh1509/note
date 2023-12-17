# JDK

# Maven

```
wget https://dlcdn.apache.org/maven/maven-3/3.8.8/binaries/apache-maven-3.8.8-bin.tar.gz -P /tmp

sudo tar xf /tmp/apache-maven-3.8.8-bin.tar.gz -C /opt

sudo ln -s /opt/apache-maven-3.8.8 /opt/maven
```

### Set Up Environment Variables

```
sudo nano /etc/profile.d/maven.sh

export JAVA_HOME=/usr/lib/jvm/jdk-17-oracle-x64
export M2_HOME=/opt/maven
export MAVEN_HOME=/opt/maven
export PATH=${M2_HOME}/bin:${PATH}

sudo chmod +x /etc/profile.d/maven.sh

source /etc/profile.d/maven.sh
```