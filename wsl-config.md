## Instalando distro Ubuntu
```bash
wsl.exe --list --online

wsl.exe --install Ubuntu
```

## Configurando git
```bash
git config --global user.name "Your Name"
```
```bash
git config --global user.email "youremail@domain.com"
```

### Configurando SSH KEY
```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```
```bash
cat ~/.ssh/id_ed25519.pub
```
Agora basta adicionar: https://github.com/settings/keys

### Configurando Docker
```bash
sudo apt install -y apt-transport-https ca-certificates curl software-properties-common

```

```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

```bash
echo "deb [signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

```bash
sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io
```

```bash
sudo usermod -aG docker $USER
```

```bash
newgrp docker
```

```bash
docker run hello-world
```

```bash
sudo apt install docker-compose
```

## Configurando Node
```bash
sudo apt update && sudo apt upgrade -y
```

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
```

```bash
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
```

```bash
nvm --version
```

```bash
nvm install --lts
```

## Configurando Java
```bash
sudo apt update
```

```bash
 sudo apt-get install curl
```

```bash
 sudo apt-get install default-jdk
```

## Configurando C# (APIS e Aplicações Console)
```bash
sudo apt update && sudo apt upgrade -y
```
```bash
sudo apt install -y wget apt-transport-https software-properties-common
```
```bash
wget https://packages.microsoft.com/config/ubuntu/24.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```
```bash
sudo apt update
sudo apt install -y dotnet-sdk-8.0
```
```bash
sudo apt install -y aspnetcore-runtime-8.0
```
