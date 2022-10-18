# ansible-tutorial
Ansible-tutorial

# Ping Example

`ansible-playbook -i hosts.yml ping.yml`

--> Was ist los? 

Für mehr Information:

`ansible-playbook -i hosts.yml -vvv ping.yml`

## Hürde - Wie fange ich an?

Ich mage keine Magie!

`ansible-config init --disabled > ansible.cfg`

- Inventar festlegen
- SSH login user festlegen (hier mein username)
- rollen default folder festlegen (Default `/roles` höchste Präzedenz)


## Assignment 1:

Copy a text file containing the words "I love ansible" to your remote host.

### Ein Playbook erstellen

Warte wie gebe ich den Pfad zu meinen Text file an?

Den ganzen Pfad?? Der wird sich doch ändern :( 


--> Rolle erstellen

`cd roles`

`ansible-galaxy init copy-files`


Option um superuser password auf der Kommandozeile zu verwenden.

`--ask-become-pass`


## Assignment 2:

Copy a text file containing the the "I love ansible from <username>" to your remote host. 

### Jinja2 Example 

Print `ansible_fact`
```yml 
- name: Print all available facts
  ansible.builtin.debug:
    var: ansible_facts
 ```

What is {{ hallo }}? 

