Etape 1:

- création du wrokspace devconteneur

- modification du devconteneur en ajoutant la ligne ci_dessous:

`postCreateCommand": "pip3 install --user --upgrade pip && pip3 install --user -r requirements.txt`

- dans le fichier requirements.txt, on ajoute:

`ansible` ==> indique l'installation de "ansible" au rebuild.

- Création du fichier ./etc/hosts.yml dans lequel on renseigne:
    
    `servers:
        hosts:
            example-server.cloud`

- Création du fichier ansible.cfg pour spécifier l'utilisateur de connexion, au server distant!
- y indiquer aussi le chemin de l'inventaire "inventory"

**NB**: On se connecte via un utilisateur definit (pas root), mais il est essentiel de passer "root" pour administrer le server. Il faut donc configurer  le fichier -> (.cfg) et on y rajoute:

    `[privilege_escalation]`

