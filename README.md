[EH Journal (E-next.in).pdf](https://github.com/user-attachments/files/33927361/EH.Journal.E-next.in.pdf)
[Artifficial Intelligence Practical Om Sem5 (1).pdf](https://github.com/user-attachments/files/33927357/Artifficial.Intelligence.Practical.Om.Sem5.1.pdf)
[TYCS - SEM - 5 - Software Testing & Quality Assurance Practical File.docx](https://github.com/user-attachments/files/33927351/TYCS.-.SEM.-.5.-.Software.Testing.Quality.Assurance.Practical.File.docx)
[Linux_Server_Administration_Practical_Handbook.docx_20260930_081600_0000.pdf](https://github.com/user-attachments/files/33927344/Linux_Server_Administration_Practical_Handbook.docx_20260930_081600_0000.pdf)
[sudo apt update.txt ppp.txt](https://github.com/user-attachments/files/33953933/sudo.apt.update.txt.ppp.txt)
sudo apt update                
sudo apt install apache2

sudo mkdir -p /var/www/site1
printf '<h1>Site 1 - Linux Lab</h1>\n' | sudo tee /var/www/site1/index.html

sudo nano /etc/apache2/sites-available/site1.conf

<VirtualHost *:80>
    ServerName site1.lab.example
    DocumentRoot /var/www/site1
    ErrorLog ${APACHE_LOG_DIR}/site1-error.log
    CustomLog ${APACHE_LOG_DIR}/site1-access.log combined
</VirtualHost>

ctrl + o enter
ctrl + x yes enter

sudo a2dissite 000-default.conf                  
sudo a2ensite site1.conf
sudo apache2ctl configtest
sudo systemctl restart apache2

curl http://site1.lab.example
