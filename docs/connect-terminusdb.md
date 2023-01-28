# How to connect dfrnt.com with TerminusDB

DFRNT.com helps you manage data products that are either hosted for you (with the subscription) or connected via API and stored at TerminusDB for the free option. To get started for free, you need to connect your data product instance(s) at TerminusDB.

There are two steps to get started: 

1. get an account, and setup a data product at TerminusDB
2. connect the data product to DFNRT.com.

## Step 1: Create your data product in TerminusX/TerminusDB

It's easiest to bring up a text editor to save the values you need for later.

1. Join the TerminusX Public Beta at [TerminusX](https://terminusdb.com/products/terminusx/)
1. Sign up for an account (Remember that the **team name** will be used later)
1. Confirm your email address
1. Login to [https://dashboard.terminusdb.com](https://dashboard.terminusdb.com) to create your **data product**
1. Create the data product (note that the id and name are not the same), you will need the data **product id** to connect Zebra
1. Create an API key for connecting DFRNT.tech to TerminusDB (upper right/profile in the menu)
1. Add a token description, generate new token and copy it

You should now have the three things you need to connect Zebra to your data product:

* A `TerminusDB Team name` (See your Profile to find it)
* A `Data Product ID` (See about the Data Product)
* The `API key` (Create one in the profile, you can create as many as you need)

## Step 2: Connect DFRNT.com to TerminusDB

1. Sign up for DFRNT.com through the sign-up on the homepage [dfrnt.com](https://dfrnt.com)
1. Once logged in to [DFRNT.com](https://dfrnt.com), go to Settings/API Keys. Or use the guided setup at `Learn More/Start Free`.
1. Add your `Settings/API Key`: Fill in the TerminusDB Team (that your captured above), "Token" and the API Token (see above)
1. Complete filling in the details for your team/instance; the setup is similar for the localhost subscription
1. Team/Instance: Fill in TerminusDB Team (connects using the server-side vaulted API token) as both team name and team reference
1. Team/Instance: Set the id to commit as, you likely want to use your email address (like you would if you use git)
1. Create a named TerminusDB connection pointer to a data product branch in your team/instance, or create a sandbox data product. In settings, this is part of the team-specific settings.
1. Pointer creation: Select your `TerminusDB Team`
1. Pointer creation: Enter your `TerminusDB data product id` (see above)
1. Pointer creation: Set the branch you want to be working on (usually `main`)

If all went well, you should now be ready to add your schema and data in the Model Editor.

If you encounter any errors, feel free to submit an issue at [Github/issues](https://github.com/dfrnt-com/support/issues). Be careful to check that you share no secret information, like the API token if you copy/paste a screenshot.
