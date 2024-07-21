# Gitpod
my sample
# Install Android SDK
sudo apt update
sudo apt install -y openjdk-11-jdk
mkdir -p ~/Android/Sdk
wget https://dl.google.com/android/repository/commandlinetools-linux-6858069_latest.zip -O cmdline-tools.zip
unzip cmdline-tools.zip -d ~/Android/Sdk/cmdline-tools
export ANDROID_SDK_ROOT=~/Android/Sdk
export PATH=$PATH:$ANDROID_SDK_ROOT/cmdline-tools/tools/bin
yes | sdkmanager --licenses
sdkmanager "platform-tools" "platforms;android-30" "build-tools;30.0.3"

# Install Android Studio
wget https://dl.google.com/dl/android/studio/ide-zips/2020.3.1.25/android-studio-2020.3.1.25-linux.tar.gz -O android-studio.tar.gz
tar -xzf android-studio.tar.gz -C ~/
export PATH=$PATH:~/android-studio/bin

# Start Android Studio
studio.sh

