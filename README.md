ssh-keygen -t ed25519 -C "mohamed_abdulnaby@icloud.com"
#to add te SSH agent
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519

#to add the public key to github
cat ~/.ssh/id_ed25519.pub
#and then copy the result to github-> settings-> SSH adn GPG keys-> New SSH key

git remote set-url origin git@github.com:mohamed-abdulnaby/Task_1.git


#to test the connection 
ssh -T git@github.com

