# Hadoop 2 Build for Windows

Unofficial Precompiled Windows build of the hadoop-releases [2.7.5 ; 2.8.3 ; 2.9.0] based on instructions in https://github.com/apache/hadoop/blob/trunk/BUILDING.txt
<br/>
Built on windows server 2016 with windows sdk 7.1 , maven 3.5.2, protocolbuffer 2.5.0 , cmake 3.10.1, zlib 1.2.11
<br/>
Note: The build in this repo excludes hadoop-2.x.x\share folder which contains bulk of the jars which can be sourced from alternate platform builds.
<br/>
# Download and Setup Hadoop Windows Binaries :
mkdir c:\hdp
<br/>
cd c:\hdp
<br/>
git clone https://github.com/jayanmuralidharan/hadoop2windowsbuild.git
<br/>
cd hadoop2windowsbuild
<br/>
Extract windows binaries
<br/>
unzip hadoop-2.x.x.zip
<br/>
# Setup Environment variables:
set HADOOP_HOME=c:\hdp\hadoop2windowsbuild\hadoop-2.x.x
<br/>
Make sure you have JDK 8 installed. Modify %HADOOP_HOME%\etc\hadoop\hadoop-env.cmd to use windows short path for the jdk folder as below:
<br/>
set JAVA_HOME=C:\Progra~1\Java\jdk1.8.0_131
<br/>

# Add rest of jar dependencies from standard build
curl -O http://apache.claz.org/hadoop/common/hadoop-2.7.5/hadoop-2.7.5.tar.gz
<br/>
tar -xzvf hadoop-2.7.5.tar.gz
<br/>
Copy over only the 'share' folder that contains the jars to the HADOOP_HOME directory
<br/>
Add %HADOOP_HOME%\bin to PATH variable.
<br/>
