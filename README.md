# PowerApps Components Framework Command Lists:

## Creating a new component project

### To create a new project:

1.  Open a **Developer Command Prompt for VS 2017 or higher** window. Create a new folder for the project using the following command:

    ```
    mkdir <folder name>
    ```

2.  Go into the component folder using the command

    ```
    cd <folder name>
    ```

3.  Create a new component project by passing basic parameters using the command

    ```
    pac pcf init --namespace <specify your namespace here> --name <name of the code component> --template <component type>
    ```

4.  Install the project build tools using the command

    ```
    npm install
    ```

5.  Open your project folder in a developer environment of your choice and get started with your code component development. The quickest way to start is by running `code .` from the command prompt once you are in the proje directory. This command opens your component project Visual Studio Code.

## Packaging your code components

### Follow these steps to create and import a solution file:

1.  Create a new folder Solutions inside the LinearComponent folder and navigate into the folder.

2.  Create a new solution project in the LinearComponent folder using the following command.

    ```
    pac solution init --publisher-name developer --publisher-prefix dev
    ```

3.  Once the new solution project is created, you need to refer to the location where the created component is located. You can add the reference by using the following command.

    ```
    pac solution add-reference --path c:\users\LinearComponent
    ```

4.  To generate a zip file from your solution project, you need to cd into your solution project directory and build the project using the following command:

    ```
    msbuild /t:restore
    ```

5.  Again, run the following command:

    ```
    msbuild
    ```
