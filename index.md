---
layout: default
---

<div style="text-align: center; margin-bottom: 30px;">
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="150 50 500 350" width="100%" style="max-height: 280px;">
    <g transform="translate(150, 80)">
      <path d="M-50,0 L550,0 M-50,100 L550,100 M-50,200 L550,200" stroke="#1c2022" stroke-width="1" />
      <path d="M0,-50 L0,350 M100,-50 L100,350 M200,-50 L200,350 M300,-50 L300,350 M400,-50 L400,350" stroke="#1c2022" stroke-width="1" />
      <path d="M 0 280 L 60 280 L 100 240 L 100 190 L 140 150 L 180 150 L 210 120" fill="none" stroke="#2c3136" stroke-width="4" stroke-linejoin="round"/>
      <path d="M 170 170 L 150 200 L 130 200 L 120 220" fill="none" stroke="#444b52" stroke-width="4" stroke-linejoin="round"/>
      <path d="M 190 155 L 195 190 L 210 210 L 205 225" fill="none" stroke="#444b52" stroke-width="3" stroke-linejoin="round"/>
      <polygon points="210,120 250,90 340,90 380,110 320,140 240,140" fill="#121417" stroke="#5c6670" stroke-width="4" stroke-linejoin="round"/>
      <path d="M 310 135 L 320 170 L 340 185 L 350 180" fill="none" stroke="#5c6670" stroke-width="4" stroke-linejoin="round"/>
      <path d="M 255 135 L 250 165 L 235 180 L 225 175" fill="none" stroke="#444b52" stroke-width="3" stroke-linejoin="round"/>
      <polygon points="340,90 390,60 460,60 420,110 380,110" fill="#181b1f" stroke="#7c8996" stroke-width="4" stroke-linejoin="round"/>
      <polygon points="430,73 438,65 446,73 438,81" fill="#39FF14"/>
      <path d="M 446 73 L 520 73" fill="none" stroke="#39FF14" stroke-width="1" stroke-dasharray="4,4" opacity="0.4"/>
    </g>
  </svg>
  <h1 style="letter-spacing: 4px; margin: 0;">CALANGOSS</h1>
  <div style="color: #39FF14; font-size: 13px; letter-spacing: 3px; font-family: monospace;">// OFFENSIVE RESEARCH</div>
</div>

<hr style="border: 0; border-top: 1px dashed #1c2022; margin: 20px 0;">

<details open>
  <summary><b>root@calangoss:~# ls -la</b></summary>
  
  <details style="margin-left: 20px; margin-top: 10px;">
    <summary><b>drwxr-xr-x /Advisories</b></summary>
    <ul style="list-style-type: square;">
      <li>
        <a href="https://nvd.nist.gov/vuln/detail/CVE-2023-3643" target="_blank"><b style="color: #ff5722;">[CVE-2023-3643]</b></a>
      </li>
    </ul>
  </details>

  <details style="margin-left: 20px; margin-top: 5px;">
    <summary><b>drwxr-xr-x /Research</b></summary>
    <ul style="list-style-type: square;">
      <li><a href="#link">t(o.ot)</a></li>
      <li><a href="#link">t(o.ot)</a></li>
    </ul>
  </details>

  <details style="margin-left: 20px; margin-top: 5px;">
    <summary><b>drwxr-xr-x /Tools</b></summary>
    <ul style="list-style-type: square;">
      <li>t(o.ot)</li>
    </ul>
  </details>

  <details style="margin-left: 20px; margin-top: 5px;">
    <summary><b>drwxr-xr-x /Writeups CTF</b></summary>
    <ul style="list-style-type: square;">
      <li>t(o.ot)</li>
      <li>t(o.ot)</li>
    </ul>
  </details>

</details>

<script>
  function downloadCode(codeBlockId, fileName) {
    const codeContent = document.getElementById(codeBlockId).innerText;
    const blob = new Blob([codeContent], { type: 'text/plain' });
    const url = URL.createObjectURL(blob);
    const a = document.createElement("a");
    a.href = url;
    a.download = fileName;
    document.body.appendChild(a);
    a.click();
    document.body.removeChild(a);
    URL.revokeObjectURL(url);
}
</script>

<br>
<br>