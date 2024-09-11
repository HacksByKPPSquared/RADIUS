Lab 20: Configuring a RADIUS server with Windows

1\. Add the Network Policy Server role

In this task, you will add the role of Network Policy Server to the
Win12R2 server. You will then add the Network Policy and Access Services
Tools.

1\. Launch the Win12R2 virtual machine to access the graphical login
screen.

2\. While on the splash screen, focus on the NETLAB+ tabs. Click the
drop-down menu for the Win12R2 tab and click on Send CTRL+ALT+DEL

3\. Log in as Administrator using the password Train1ng\$.

> <img src="./media/image1.png" style="width:3.98611in;height:1.59722in"
> alt="A person in a lab coat Description automatically generated" />
>
> 4\. Notice a Server Manager window appears upon bootup. In the Server
> Manager window, click on Manage in the top-right corner and select Add
> Roles and Features.
>
> <img src="./media/image2.png" style="width:6.14302in;height:3.45545in"
> alt="A screenshot of a computer Description automatically generated" />
>
> 5\. Notice the Add Roles and Features Wizard appears. Review the
> Before you begin page and click Next to
> continue.<img src="./media/image3.png" style="width:5.98611in;height:4.26389in"
> alt="A screenshot of a computer program Description automatically generated" />
>
> 6\. n the Installation Type step, keep the default setting of
> Role-based or featurebased Installation and click Next.
>
> <img src="./media/image4.png" style="width:5.94444in;height:5.40278in"
> alt="A screenshot of a computer Description automatically generated" />

7\. On the Server Selection step, select the Win12R2.lab.local server
from the pool and click Next.

> <img src="./media/image5.png" style="width:5.95833in;height:5.38889in"
> alt="A screenshot of a computer Description automatically generated" />
>
> 8\. On the Server Roles step, check the checkbox for Network Policy
> and Access Services and notice a pop-up window appears. Click the Add
> Features button.
>
> <img src="./media/image6.png" style="width:3.22222in;height:3.34722in"
> alt="A screenshot of a computer Description automatically generated" />
>
> 9\. Back on the main wizard window, ensure that Network Policy and
> Access Services is checked and click Next.
>
> <img src="./media/image7.png" style="width:5.95833in;height:5.375in"
> alt="A screenshot of a computer Description automatically generated" />

10\. On the Features step, leave the defaults and click Next.

<img src="./media/image8.png" style="width:6.02778in;height:5.40278in"
alt="A screenshot of a computer Description automatically generated" />

11\. On the Network Policy and Access Services step, review the
information and click Next.

<img src="./media/image9.png" style="width:5.98611in;height:5.25in"
alt="A screenshot of a computer Description automatically generated" />

12\. On the Role Services step, ensure that Network Policy Server is
checked and click Next.

<img src="./media/image10.png" style="width:5.95833in;height:5.375in"
alt="A screenshot of a computer Description automatically generated" />

13\. On the Confirmation step, click Install to finish the installation
of the Network Policy Server.

> 14\. The installation will take about 3 minutes. After the install is
> complete, click Close.
> <img src="./media/image11.png" style="width:5.94444in;height:5.38889in"
> alt="A screenshot of a computer Description automatically generated" />

15\. Leave the Win12R2 window open to continue with the next task.

2\. Configure the Network Policy Server

1\. Back on the Server Manager window, navigate to Tools \> Network
Policy Server.

<img src="./media/image12.png" style="width:3.375in;height:4.84722in"
alt="A screenshot of a computer Description automatically generated" />

2\. In the Network Policy Server window, in the left pane, right-click
on NPS (Local) and select Register Server in Active Directory.

<img src="./media/image13.png" style="width:2.27778in;height:2.43056in"
alt="A screenshot of a computer Description automatically generated" />

3\. When prompted to authorize, click OK to continue.

<img src="./media/image14.png" style="width:3.69444in;height:1.73611in"
alt="A computer screen shot of a computer Description automatically generated" />

4\. Click OK again to confirm that the system is now authorized.

<img src="./media/image15.png"
style="width:3.68056in;height:1.72222in" />

5\. Expand the RADIUS Clients and Servers inventory object, right-click
on RADIUS Clients and click New.

<img src="./media/image16.png" style="width:1.54167in;height:1.86111in"
alt="A screenshot of a computer Description automatically generated" />

6\. In the New RADIUS Client window, fill in the following information:
a. Friendly name: Windows Client b. Address: 192.168.1.100 c. Shared
secret: password123 d. Confirm shared secret: password123

<img src="./media/image17.png" style="width:3.55556in;height:4.43056in"
alt="A screenshot of a computer Description automatically generated" />

7\. Once the configurations are made, click OK.

8\. Select RADIUS Clients from the left pane and verify that Windows
Client appears in the right pane and that it is enabled.

<img src="./media/image18.png" style="width:5.91667in;height:1.72222in"
alt="A screenshot of a computer Description automatically generated" />

9\. Now it is time to create a new network policy. In the left pane,
expand Policies, right-click on Network Policies and select New.

<img src="./media/image19.png" style="width:1.73611in;height:2.58333in"
alt="A screenshot of a computer Description automatically generated" />

10\. In the New Network Policy window, type Remote Access RADIUS in the
Policy name text field and click Next.

<img src="./media/image20.png" style="width:3.29703in;height:2.85028in"
alt="A screenshot of a computer Description automatically generated" />

11\. On the Specify Conditions step, click the Add button.

<img src="./media/image21.png" style="width:3.62376in;height:2.61338in"
alt="A screenshot of a computer Description automatically generated" />

12\. In the Select condition window, scroll down and select Access
Client IPv4 Address and click Add.

<img src="./media/image22.png" style="width:5.125in;height:0.81944in"
alt="A screen shot of a computer Description automatically generated" />

13\. When prompted for an IPv4 address, type 192.168.1.100 and click OK.

<img src="./media/image23.png" style="width:3.11111in;height:1.375in"
alt="A screenshot of a computer Description automatically generated" />

14\. Back on the Specify Conditions step, ensure that the new condition
is listed and click Next.

<img src="./media/image24.png" style="width:5.11111in;height:4.45833in"
alt="A screenshot of a computer Description automatically generated" />

15\. On the Specify Access Permission step, leave the Access granted
selected and click Next.

<img src="./media/image25.png" style="width:5.15278in;height:4.48611in"
alt="A screenshot of a computer Description automatically generated" />

16\. On the Configure Authentication Methods step, leave the default
settings and click Next.

<img src="./media/image26.png"
style="width:3.61401in;height:3.16832in" />

17\. On the Configure Constraints step, leave the default settings and
click Next.

<img src="./media/image27.png" style="width:4.37624in;height:3.77948in"
alt="A screenshot of a computer Description automatically generated" />

18\. On the Configure Settings step, leave the defaults and click Next.

<img src="./media/image28.png" style="width:5.25in;height:4.52778in"
alt="A computer screen shot of a computer Description automatically generated" />

19\. On the Completing New Network Policy step, click Finish. You now
have a new network policy for the RADIUS client.

<img src="./media/image29.png" style="width:5.23611in;height:4.56944in"
alt="A screenshot of a computer Description automatically generated" />

20\. Back on the Network Policy Server window, in the left pane, click
on Network Policies and confirm the new policy appears in the right
pane.

<img src="./media/image30.png" style="width:5.875in;height:1.27778in"
alt="A screenshot of a computer Description automatically generated" />

21\. The lab is now complete; you may end the reservation.
