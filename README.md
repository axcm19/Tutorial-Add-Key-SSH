1 - Open terminal.

-----------------------------------------------------------------------------------------------------------------------------------------------------------

2 - Paste the text below, substituting in your GitHub email address.

      $ ssh-keygen -t ed25519 -C "your_email@example.com"
      
-----------------------------------------------------------------------------------------------------------------------------------------------------------
      
3 -  This creates a new SSH key, using the provided email as a label.

      > Generating public/private ALGORITHM key pair.

-----------------------------------------------------------------------------------------------------------------------------------------------------------

4 - When you're prompted to "Enter a file in which to save the key", you can press Enter to accept the default file location. Please note that if you
created SSH keys previously, ssh-keygen may ask you to rewrite another key, in which case we recommend creating a custom-named SSH key. To do so, type the
default file location and replace id_ssh_keyname with your custom key name.

      > Enter passphrase (empty for no passphrase): [Type a passphrase]
      > Enter same passphrase again: [Type passphrase again]
      
-----------------------------------------------------------------------------------------------------------------------------------------------------------

5 - Start ssh-agent in second plan. 

      $ eval "$(ssh-agent -s)"
      > Agent pid 59566
      
-----------------------------------------------------------------------------------------------------------------------------------------------------------

6 - Add your SSH private key to the ssh-agent. If you created your key with a different name or if you are adding an existing key that has another name,
replace id_ed25519 in the command with the name of the private key file.

      $ ssh-add ~/.ssh/id_ed25519

-----------------------------------------------------------------------------------------------------------------------------------------------------------

7- Copy the SSH public key to your clipboard.

      $ cat ~/.ssh/id_ed25519.pub
        
Then select and copy the contents of the id_ed25519.pub file displayed in the terminal to your clipboard.

-----------------------------------------------------------------------------------------------------------------------------------------------------------

8- Go to Github in "Settings/SSH keys/New SSH Key" and copy content from terminal after executing previous comand.












