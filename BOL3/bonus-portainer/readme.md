
  docker run -d \
  -p 9000:9000 \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v portainer_data:/data \
  --name portainer \
  portainer/portainer-ce

* ce= comunity edition 

  - Portainer, Docker Desktop’ın kendi çalıştırdığı Docker Engine’e Unix socket üzerinden bağlanır:
  * /var/run/docker.sock

  	* Portainer, direkt Docker Engine ile konuşur
	•	Docker Desktop’taki tüm container, image, network, volume’ları görür
	•	Tam erişim, tam yönetim
Docker Desktop, Linux VM içinde Docker Engine çalıştırır ama host tarafında socket’i expose eder.

-  UI’dan bağladığında:

- Portainer UI’da:

- environments → Add Environment → Docker Standalone → Local seçilir.
- Portainer otomatik olarak socket bağlantısını görür.




docker restart portainer