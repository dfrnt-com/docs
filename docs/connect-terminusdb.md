# How to connect dfrnt.tech with TerminusDB

DFRNT.tech relies on TerminusDB as the backing data mesh, where your data is stored. To build your data mesh, you need a data product at TerminusDB.

There are two steps to get started: 

1. setup a data product at TerminusDB
2. connect the data product to DFNRT.tech.

## How to create your data product in TerminusX/TerminusDB

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

## Connect Zebra to TerminusDB

1. Sign up for Zebra through the sign-up/invitation link you received
1. Once logged in to [DFRNT.tech](https://dfrnt.tech), go to Settings/API Keys
1. Add your `Settings/API Key`: Fill in the TerminusDB Team (that your captured above), "Token" and the API Token (see above)
1. Add TerminusDB connection in `Settings/Workspaces`
  1. Add TerminusX Team: Fill in TerminusDB Team (connects using the server-side vaulted API token) as both team name and team reference
  1. Set your commit id, your likely want to use your email address (like you would if you use git)
1. Create a DFRNT.tech workspace and menu entry for it
  1. Select your `TerminusDB Team`
  1. Enter your `TerminusDB data product id` (see above)
  1. Set the branch you want to be working on (usually `main`)

If all went well, you should now be ready to add your schema and data in the Model Editor.

If you encounter any errors, feel free to submit an issue at [Github/issues](https://github.com/dfrnt-com/support/issues). Don't share any secret information though, like the API token.
