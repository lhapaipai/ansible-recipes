## Prérequis sur un nouveau serveur dédié avant de lancer le playbook

générer un mot de passe à l'utilisateur root et ajouter la clé publique à `/root/.ssh/authorized_keys`.

```bash
# ~/.ssh/config
Host <alias>
  HostName <server-ip-hostname>
  Port 22
  User <admin-user>
```

```bash
ssh-copy-id -i .ssh/<your-pub-key>.pub <alias>
```

```bash
# pour une connexion root
ssh <alias>
sudo su
cat .ssh/authorized_keys >> /root/.ssh/authorized_keys
```