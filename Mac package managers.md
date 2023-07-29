## Homebrew
you know it ;)

## NVM (Node)
Node Version Manager (NVM) is a tool that allows you to download and install Node.js versions. It lets you easily switch between Node.js versions, which is essential for testing your application on different Node.js environments.

Here is a step-by-step guide on how to install NVM and use it to manage Node.js versions:

1. **Installing NVM**:
   - Open a terminal.
   - Install NVM by copying and pasting the following command and hitting enter:
     ```bash
     curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
     ```
     The above command will download a script and run it. This script will clone the NVM repository to `~/.nvm`, and it will add the source lines to your profile (`~/.bash_profile`, `~/.zshrc`, `~/.profile`, or `~/.bashrc`).

2. **Verifying the Installation**:
   - Close the terminal and open a new one.
   - Verify the installation by running:
     ```bash
     command -v nvm
     ```
     If the `nvm` command is not found, you might need to either open a new terminal or manually add the NVM scripts to your `~/.bash_profile`, `~/.zshrc`, `~/.profile`, or `~/.bashrc`.

3. **Installing Node.js versions**:
   - To install a specific version of Node.js, you can use `nvm install <version>`. For example, to install Node.js 14.15.1, you would use:
     ```bash
     nvm install 14.15.1
     ```
   - If you want to install the latest version, you can use:
     ```bash
     nvm install node
     ```
   - If you want to install the latest LTS (Long Term Support) version, you can use:
     ```bash
     nvm install --lts
     ```

4. **Switching between Node.js versions**:
   - You can switch between installed versions using `nvm use <version>`. For example:
     ```bash
     nvm use 14.15.1
     ```
   - You can also alias specific versions. For instance, if you always want to refer to version 14.15.1 as "prod", you could use:
     ```bash
     nvm alias prod 14.15.1
     ```
     Then, you could switch to it with `nvm use prod`.

5. **Uninstalling Node.js versions**:
   - If you want to uninstall a specific version, you can use `nvm uninstall <version>`. For example:
     ```bash
     nvm uninstall 14.15.1
     ```

Note: Each version of Node.js comes with its own npm, so when you switch between Node.js versions, you're also switching npm versions.

NVM does not explicitly manage NPM versions (beyond the version that comes with each Node.js version). If you want to install a specific version of NPM for a specific Node.js version, you can do so using npm itself:

```bash
npm install -g npm@6.14.8
```

To view the versions of Node and NPM currently in use, you can use `node -v` and `npm -v` respectively.

With these steps, you can manage different versions of Node.js and npm using NVM. This is particularly useful when you're developing applications that need to run on different Node.js environments.

## SDKMAN! (Java)
Using Apple Silicon Mac, you can install and manage Java versions using SDKMAN!. It's a versatile tool, managing not just multiple Java versions but also other SDKs like Gradle, Maven, Scala, Kotlin, etc. SDKMAN! is especially recommended if you need to frequently switch between different Java versions. 

Here are the steps you need to follow:

1. Open Terminal.

2. Install SDKMAN! with the following command:
    ```bash
    curl -s "https://get.sdkman.io" | bash
    ```
   
3. Open a new Terminal window or source the installed files:
    ```bash
    source "$HOME/.sdkman/bin/sdkman-init.sh"
    ```
   
4. Confirm that the installation was successful by checking the version of SDKMAN!:
    ```bash
    sdk version
    ```
   
5. Now, you can install Java. To get a list of all the available versions, use:
    ```bash
    sdk list java
    ```
   
6. You'll see a variety of Java versions, including versions optimized for Apple M1 (like Zulu and GraalVM distributions). To install a version, use `sdk install java <version>`. For example, to install Azul's Zulu OpenJDK 17 for M1, use:
    ```bash
    sdk install java 17.0.0-zulu
    ```
   
7. The installed version will be the new default. You can switch between installed versions using the `sdk use` command, e.g., `sdk use java 17.0.0-zulu`.

8. You can view where Java is installed by using the `which java` command in the terminal. 

9. SDKMAN! will prevent duplicate version installations and help save your computer storage.

In this way, you can ensure that you have a reliable Java installation where all the necessary tools are installed, and you can also switch between versions without a headache. SDKMAN! provides the best way to install Java on an Apple Silicon Mac, considering your requirements.
