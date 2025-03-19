# Lab 1: Bot Protection
We usually do sales promotions in our websites, but always we put a product with low price, it sold out very quickly and the "customer" cancel the order few days later... We lost the revenue and our other customers are complaining because they cannot buy it...

Maybe are these "customers" bots? Can you help us to see if we have a bot-proof website?

## Task 1 - Proof of concept
1. Let's see if the a bot could be run against our website. Access Kali VNC using the public IP from Student Resources.
**https://kali-pip/vnc.html**

2. Accept certificate errors and proceed. When prompted, click **Connect**. 

3. At the top of the page, click on the terminal icon (black box). Once open, input:

    ``` 
    vim /simple_ff.py
    ```

    !!! tip
        Note: If you are not familiarized with VIM, some commands can be useful: use INSERT to start editing the file. To exit saving the file: ESC then type ```wq!``` and ENTER. To exit without saving: ESC then type ```q!``` and ENTER

        ![lab1 botpr img1](lab1-botpr-img1.png)


4. Replace the XXXXX with your FortiWeb Public IP

    ![lab1 botpr img2](lab1-botpr-img2.png)

5. With the file changed and saved, type:

    ``` 
    python3 /simple_ff.py
    ```

    ![lab1 botpr img3](lab1-botpr-img3.png)

6. It will open Firefox and the bot will start running.

    ![lab1 botpr img4](lab1-botpr-img4.png)

7. You will see it "clicking" in the webpage products, creating new user, adding address, payment options, adding items to the basket (shopping cart) and checking out. Wait for it completes all the tasks. When done it will show you in the terminal:

    ![lab1 botpr img5](lab1-botpr-img5.png)

## Task 2 - End bot's party
1. Ok... we know bots can use our website... let's learn one way that we can block them. Open **FortiWeb** and go to **Bot Mitigation** > **Biometrics Based Detection**. Click **Create New**

    ![lab1 botpr img6](lab1-botpr-img6.png)

2. Fill like we shown below and click **Ok**:

    ![lab1 botpr img7](lab1-botpr-img7.png)

3. In the same page, now click **Create New**. Fill the fields as shown below and then click **OK** twice

    ![lab1 botpr img8](lab1-botpr-img8.png)

4. Click **Bot Mitigation Policy** menu and then **Create New**

    ![lab1 botpr img9](lab1-botpr-img9.png)

5. Make yours look like below and click **OK**

    ![lab1 botpr img10](lab1-botpr-img10.png)

6. Now, go to **Policy** > **Server Policy** and double click **SP_JuiceShop**
    ![lab1 botpr img11](lab1-botpr-img11.png)
7. Scroll down to **Web Protection Profile**, click on it and then click **Create**
    ![lab1 botpr img12](lab1-botpr-img12.png)

8. Name it as **WP_JuiceShop**

    ![lab1 botpr img13](lab1-botpr-img13.png)

9. Scroll down to **Bot Mitigation Policy** and select the one created earlier. Click **OK**. Make sure the new **Web Protection Profile** is selected and click **Ok** again

    ![lab1 botpr img14](lab1-botpr-img14.png)
    ![lab1 botpr img18](lab1-botpr-img18-mg.png)

10. Go back to your Kali terminal and run the same command again

    ```
    python3 /simple_ff.py
    ```

11. Firefox will open and perform the same tasks again. However, this time it will stop in some step, like the one below

    ![lab1 botpr img15](lab1-botpr-img15.png)

12. Minimize Firefox and go back to Kali terminal, you will see errors similar to these:

    ![lab1 botpr img16](lab1-botpr-img16.png)

13. Go back to Firefox and update the page (CTRL+R) you will see FortiWeb block message

    ![lab1 botpr img17](lab1-botpr-img17.png)

    !!! warning
        Important: If you don't see the error/block message after the first time, it could be the FortiWeb learning from the behavior. Try it twice more.

14. This was one way to block bot based on biometrics, but FortiWeb is rich of features to fight against them, including a ML special for bot protection


