<p align="center">
    <img height="140" src="https://user-images.githubusercontent.com/35038240/221522083-1011e567-e2b7-424c-a018-15e965cf8df9.png#gh-light-mode-only">
    <img height="140" src="https://user-images.githubusercontent.com/35038240/221522077-5b1e3eca-ca85-4c9f-93a9-afd39cc93c88.png#gh-dark-mode-only">
</p>

## What's JPRQ?

- JPRQ is a free and open tool for exposing local servers to public network (the internet)
- it can expose TCP protocols, such as HTTP, SSH, major databases (MySQL, Postgres, Redis)

---

## How to install

<details>
<summary>Windows</summary>
<p align='center'><a href="https://youtube.com/watch?v=frgVQPi-GlY">📹Video tutorial</a><br></p>

1. Install the latest <a href='https://github.com/azimjohn/jprq/releases'>release</a> of JPRQ<br>
2. Place the file where it is convenient for you<br><br>
<i>(At this point, you can use the program, but you will need to manually call the <code>.exe</code> file)</i><br>
3. Create <b>jprq.bat</b> file so we can use the "jprq" keyword to call the <b>.exe</b> file<br>
    
    ```bash
    @echo off
    "C:\Exact\Path\To\File\jprq-windows-386.exe" %*
    ```

4. Awesome! Finally, we need to <a href="https://www.youtube.com/watch?v=gb9e3m98avk">add to the environment variable "PATH"</a>, the path to the folder where we created .bat file <i>(step 3)</i><br><br>
<p align='center'><b>Congratulations!</b> You can check if everything is working with the jprq command in CMD</p>
<hr>
    
</details>

<details>
    <summary> MacOs and Linux</summary>

```bash
curl -fsSL https://jprq.io/install.sh | sudo bash
```
</details>

## How to use

First obtain auth token from https://jprq.io/auth, then

```bash
jprq auth <your-auth-token>
```

Replace 8000 with the port you want to expose

```bash
jprq http 8000
```

For exposing any TCP servers, such as SSH

```bash
jprq tcp 22
```

For using custom subdomains
```bash
jprq http 3000 -s custom
```

For using jprq debugger (with v2.1 or higher)
```bash
jprq http 3000 --debug
```

Press Ctrl+C to stop it

<a href="https://www.buymeacoffee.com/azimjon" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/default-orange.png" alt="Buy Me A Coffee" height="41" width="174"></a>
