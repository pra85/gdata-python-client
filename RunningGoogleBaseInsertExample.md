# Introduction #

These instructions will guide you through running the example script which illustrates requesting a test insertion of a new item. The item will not be inserted into Google Base.

# Details #

## Execution Environment ##

Make sure that the required modules are in your Python Path. See DependencyModules for a list of things you may need to install.

## Running the example ##

You can run the example from the main project directory by executing `python samples/base/dryRunInsert.py`.

You will be prompted for a username and password.

The script will request a test insertion of a hard coded item and then display the item which would have been added to Google Base had the dry-run URL parameter not been set to true.

After displaying the server's response the script will exit.