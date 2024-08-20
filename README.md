# TB3_ws
This is the full archive of the workspace built on ubunt22.04 , ROS2 humble.   

Uploaded because the build took a long time due to low memory.  

Repository cloning is recommended for the following people,  

1. whose builds are not progressing by more than 28% in 5 hours due to low memory
2. cannot swap memory due to insufficient storage

| RasPi                | Micro SD                 | BUILD     |  
|----------------------|----------------------|----------------------|
| RasPi3                  | 16Gib                   | X      | 
| RasPi3                  | 256Gib                   | X       | 
| RasPi4                  | 256Gib                   | O       |

*USB Keyboard is working!*

---
*다운로드 받으려는 경로로 이동*
<pre>
<code id="code-block">
cd ~/turtlebot3_ws
</code>
</pre>
<button onclick="copyToClipboard()"></button>

---
*빌드 완료된 파일 다운로드*
<pre>
<code id="code-block">
git clone https://github.com/oosuiw/TB3_ws.git
</code>
</pre>
<button onclick="copyToClipboard()"></button>

*다운로드 받은 폴더로 이동*
<pre>
<code id="code-block">
cd TB3_ws/
</code>
</pre>
<button onclick="copyToClipboard()"></button>

---

*다운로드 받은 파일를 상위 폴더로 이동*
<pre>
<code id="code-block">
sudo mv build.tar.xz /home/ubuntu/turtlebot3_ws/
</code>
</pre>
<button onclick="copyToClipboard()"></button>

<pre>
<code id="code-block">
sudo mv install.tar.xz /home/ubuntu/turtlebot3_ws/
</code>
</pre>
<button onclick="copyToClipboard()"></button>

<pre>
<code id="code-block">
sudo mv log.tar.xz /home/ubuntu/turtlebot3_ws/
</code>
</pre>
<button onclick="copyToClipboard()"></button>

---

다시 상위폴더로 이동..

<pre>
<code id="code-block">
cd ..
</code>
</pre>
<button onclick="copyToClipboard()"></button>

---

비어있는 폴더는 삭제!
  
<pre>
<code id="code-block">
sudo rm -r TB3_ws
</code>
</pre>
<button onclick="copyToClipboard()"></button>

---

다운로드 받고 이동시킨 파일 압축해제하는 과정..

<pre>
<code id="code-block">
tar xvf build.tar.xz
</code>
</pre>
<button onclick="copyToClipboard()"></button>

<pre>
<code id="code-block">
tar xvf install.tar.xz
</code>
</pre>
<button onclick="copyToClipboard()"></button>

<pre>
<code id="code-block">
tar xvf log.tar.xz
</code>
</pre>
<button onclick="copyToClipboard()"></button>
  

---

*압축풀고 필요없어진 파일 삭제하는 과정..(선택사항)*

<pre>
<code id="code-block">
sudo rm build.tar.xz 
</code>
</pre>
<button onclick="copyToClipboard()"></button>

<pre>
<code id="code-block">
sudo rm install.tar.xz 
</code>
</pre>
<button onclick="copyToClipboard()"></button>

<pre>
<code id="code-block">
sudo rm log.tar.xz 
</code>
</pre>
<button onclick="copyToClipboard()"></button>


===

**여기부터는 환경 셋업!**

*아래의 숫자(=30) 다른 사람과 중복안됨! 겹치지 않는 숫자로..*
<pre>
<code id="code-block">
echo 'export ROS_DOMAIN_ID=30 #TURTLEBOT3' >> ~/.bashrc 
</code>
</pre>
<button onclick="copyToClipboard()"></button>


<pre>
<code id="code-block">
echo 'source /opt/ros/humble/setup.bash' >> ~/.bashrc
</code>
</pre>
<button onclick="copyToClipboard()"></button>


<pre>
<code id="code-block">
echo 'source ~/turtlebot3_ws/install/setup.bash' >> ~/.bashrc
</code>
</pre>
<button onclick="copyToClipboard()"></button>

---

*이번엔 직접 bashrc파일 수정하는 시간, TOP <-> BOT 간 연결하는 과정*

---

**<REMOTE_PC = 노트북(TOP)>**

<pre>
<code id="code-block">
export ROS_IP=노트북 IP
export ROS_MASTER_URI=http://localhost:11311
export ROS_HOSTNAME=$ROS_IP
</code>
</pre>
<button onclick="copyToClipboard()"></button>

**<TurtleBot3 SBC, = 로봇(BOT)>**
<pre>
<code id="code-block">
export ROS_MASTER_URI=https://노트북 IP:11311
export ROS_HOSTNAME=로봇 IP
</code>
</pre>
<button onclick="copyToClipboard()"></button>


