Setting up a EC2 instance
==========================

Go to http://aws.amazon.com/, in a Web browser.

Select 'My Account/Console' on the top right if you already have an account; otherwise sign up with a new account.

Go to the 'AWS Management Console' option, click the 'EC2' at upper left.

Before importing the AMI, make sure you are in the right Availability zone. Amazon EC2 is hosted in multiple locations world-wide with multiple Availability zones, and resources cannot replicated across regions until specified.  Our AMI is stored at region "US East(N. Virginia)". Check the upper right corner next to your account name, and make sure it's set at the right region. If not, just click and select the right one on from the dropdown menu.

Next, click the blue button 'Launch Instance'.

Step-1: Choosing the instance
-----------------------------

Click the Community AMIs tab at mid-left and simply search "viramp"

.. image:: viramp-doc/search-ami.png

Step-2: Review Instance type
-----------------------------

Due to storage and computational requirements, free tier instances are not usable with our AMI. For trial runs it is possible to choose smaller instance types, but for serious usage, it is advised to select at least the m3.large (third option)

.. image:: viramp-doc/review-instance-type.png

Step-3: Launch the Instance
-----------------------------
.. image:: viramp-doc/review-and-launch.png

Step-4: Create Key-pairs
-----------------------------
.. image:: viramp-doc/key-pair.png

Congratulations you have successfully launched your own version of the instance.  For information on logging in and starting your instance, please go to :ref:`VirAmp instance login <viramp_login_ref>`
