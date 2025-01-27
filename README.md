# CVE-2024-1561 Nuclei Template

This Nuclei template is designed to detect the Gradio CVE-2024-1561 vulnerability in web applications. Gradio is a Python library for creating customizable UI components around machine learning models. This vulnerability may allow attackers to read files from the server.


###  Running the template

Clone this repository to your local machine and run using the `-t` flag:

```bash
git clone https://github.com/DiabloHTB/Nuclei-Template-CVE-2024-1561
cd Nuclei-Template-CVE-2024-1561
nuclei -target <URL> -t CVE-2024-1561.yaml
```

Example:
```bash
┌──(gradio-env)─(diablo㉿diablo)-[~/gradio]
└─$ nuclei -target http://127.0.0.1:7860 -t CVE-2024-1561.yaml 

                     __     _
   ____  __  _______/ /__  (_)
  / __ \/ / / / ___/ / _ \/ /
 / / / / /_/ / /__/ /  __/ /
/_/ /_/\__,_/\___/_/\___/_/   v3.2.6

                projectdiscovery.io

[INF] Current nuclei version: v3.2.6 (outdated)
[INF] Current nuclei-templates version: v9.8.6 (latest)
[WRN] Scan results upload to cloud is disabled.
[INF] New templates added in latest release: 65
[INF] Templates loaded for current scan: 1
[WRN] Loading 1 unsigned templates for scan. Use with caution.
[INF] Targets loaded for current scan: 1
[CVE-2024-1561] [http] [high] http://127.0.0.1:7860/file=/tmp/gradio/83bbb89b677a9cca3d271a392fa1aa2a10853c32/passwd

```

### PoC
The template tests for `/etc/passwd` presence matching with `root` user.
To fully exploit the target check the following :   

https://huntr.com/bounties/4acf584e-2fe8-490e-878d-2d9bf2698338

https://github.com/DiabloHTB/CVE-2024-1561




Disclaimer
This template is provided for educational and informational purposes only. Usage of this template for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state, and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this template.



