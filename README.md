# rabbitmq-test

1. **Update Package List:**
   Before installing any new software, it's a good practice to update the package list to ensure you get the latest versions available.

   ```bash
   sudo apt update
   ```

2. **Install RabbitMQ:**
   RabbitMQ is available in the official Ubuntu repositories. You can install it using the following command:

   ```bash
   sudo apt install rabbitmq-server
   ```

3. **Enable and Start RabbitMQ Service:**
   The RabbitMQ service should start automatically after installation, but you can ensure it's enabled and running using the following commands:

   ```bash
   sudo systemctl enable rabbitmq-server
   sudo systemctl start rabbitmq-server
   ```

4. **Check RabbitMQ Status:**
   You can check the status of the RabbitMQ service to verify that it is running without any issues:

   ```bash
   sudo systemctl status rabbitmq-server
   ```

   If RabbitMQ is running properly, you should see an output indicating that the service is active and running.

5. **Configure RabbitMQ:**
   By default, RabbitMQ comes with a guest user, but it's a good practice to create a new user for security reasons. You can do this using the following command:

   ```bash
   sudo rabbitmqctl add_user your_username your_password
   ```

   Replace `your_username` and `your_password` with the desired username and password.

6. **Set Permissions:**
   After creating the user, you should set the necessary permissions. For example, you can grant administrative privileges to the new user:

   ```bash
   sudo rabbitmqctl set_user_tags your_username administrator
   ```

7. **Access RabbitMQ Management Console (Optional):**
   RabbitMQ comes with a web-based management console that you can access in a web browser. To enable it, use the following command:

   ```bash
   sudo rabbitmq-plugins enable rabbitmq_management
   ```

   Now, you can access the management console by visiting `http://your_server_ip:15672` in a web browser. Log in using the username and password you created or use default(guest).


We will also need to install the pika library. (https://pypi.org/project/pika/)
```bash
   pip install pika
```

- http://localhost:15672
- username: guest
- password: guest

Links:
- Official page: https://rabbitmq.com
- Concepts: https://rabbitmq.com/documentation.html
- Hands-on: https://youtu.be/av9DJkyN_8M?si=NWk8RRCOxNL6lXZB
