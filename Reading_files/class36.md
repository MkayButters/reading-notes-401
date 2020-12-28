## API Deployment

- __Different environments__. Usually, you have several environments: local, dev, ci, qa, staging, production, etc. Each environment can have its own specific settings (for example: DEBUG = True, more verbose logging, additional apps, some mocked data, etc). You need an approach that allows you to keep all these Django setting configurations.

-__Sensitive data__. You have SECRET_KEY in each Django project. On top of this there can be DB passwords and tokens for third-party APIs like Amazon or Twitter. This data cannot be stored in VCS.

- __Sharing settings between team members__. You need a general approach to eliminate human error when working with the settings. For example, a developer may add a third-party app or some API integration and fail to add specific settings. On large (or even mid-size) projects, this can cause real issues.

- __Django settings are a Python code__. This is a curse and a blessing at the same time. It gives you a lot of flexibility, but can also be a problem – instead of key-value pairs, settings.py can have a very tricky logic.

- Sharing settings between team members. You need a general approach to eliminate human error when working with the settings. For example, a developer may add a third-party app or some API integration and fail to add specific settings. On large (or even mid-size) projects, this can cause real issues.

- Django settings are a Python code. This is a curse and a blessing at the same time. It gives you a lot of flexibility, but can also be a problem – instead of key-value pairs, settings.py can have a very tricky logic.
 
> Pros:
 - Secrets not in VCS.

> Cons:
 - settings_local.py is not in VCS, so you can lose some of your Django environment settings.
 - The Django settings file is a Python code, so settings_local.py can have some non-obvious logic.
 - You need to have settings_local.example (in VCS) to share the default configurations for developers.


- Naming of variables is one of the most complex parts of development. So is naming of settings. We can’t imply on Django or third-party applications, but we can follow these simple rules for our custom (project) settings:

    - Give meaningful names to your settings.
    - Always use the prefix with the project name for your custom (project) settings.
    - Write descriptions for your settings in comments.

- Keep settings in environment variables.
- Write default values for production configuration (excluding secret keys and tokens).
- Don’t hardcode sensitive settings, and don’t put them in VCS.
- Split settings into groups: Django, third-party, project.
- Follow naming conventions for custom (project) settings.

SSH, or Secure Shell, is a remote administration protocol that allows users to control and modify their remote servers over the Internet. The service was created as a secure replacement for the unencrypted Telnet and uses cryptographic techniques to ensure that all communication to and from the remote server happens in an encrypted manner. It provides a mechanism for authenticating a remote user, transferring inputs from the client to the host, and relaying the output back to the client.

The Figure Below shows a typical SSH Window. Any Linux or macOS user can SSH into their remote server directly from the terminal window. Windows users can take advantage of SSH clients like Putty.  You can execute shell commands in the same manner as you would if you were physically operating the remote computer.

- If you’re using Linux or Mac, then using SSH is very simple. If you use Windows, you will need to utilize an SSH client to open SSH connections. The most popular SSH client is PuTTY

- The SSH key command instructs your system that you want to open an encrypted Secure Shell Connection. {user} represents the account you want to access. For example, you may want to access the root user, which is basically synonymous for system administrator with complete rights to modify anything on the system. {host} refers to the computer you want to access. This can be an IP Address (e.g. 244.235.23.19) or a domain name (e.g. www.xyzdomain.com).

- When you hit enter, you will be prompted to enter the password for the requested account. When you type it in, nothing will appear on the screen, but your password is, in fact being transmitted. Once you’re done typing, hit enter once again. If your password is correct, you will be greeted with a remote terminal window.

- The significant advantage offered by SSH over its predecessors is the use of encryption to ensure secure transfer of information between the host and the client. Host refers to the remote server you are trying to access, while the client is the computer you are using to access the host. There are three different encryption technologies used by SSH:

    1. Symmetrical encryption
    2. Asymmetrical encryption
    3. Hashing.


- The way SSH works is by making use of a client-server model to allow for authentication of two remote systems and encryption of the data that passes between them.

- SSH operates on TCP port 22 by default (though this can be changed if needed). The host (server) listens on port 22 (or any other SSH assigned port) for incoming connections. It organizes the secure connection by authenticating the client and opening the correct shell environment if the verification is successful.

[<===BACK](../README.md)
