# VPC

![img.png](other_images/image.png)

![img.png](other_images/image-1.png)


### Step 1

Navigate to the VPC console, and select create VPC.

What have we done here? We've just set up the foundation for our walls.

![img.png](other_images/image-2.png)

# Subnets

Set up my three subnets: 2 public, one private.

![img.png](other_images/image-3.png)

# Internet Gateway:

I created the doorway into this VPC for the wider internet.

![img.png](other_images/image-4.png)

# Route Table:

I created Public Route Table and associated them to direct this traffic from the Internet Gateway into my public subnets. I allowed traffic to come from everywhere. This is because it'll only be going to my web page.

![img.png](other_images/image-5.png)

Simpler diagram:

![img.png](images/user_map.png)

## Database Setup:

Set this up manually so it has a static IP address that all my later machines can connect to, as they have specific commands.

![img.png](other_images/db_setup.png)