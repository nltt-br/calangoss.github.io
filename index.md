---
layout: default
---

- ## Init
  
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
<a href="https://www.linkedin.com/company/calangos-security/" target="_blank"><img src="/assets/images/calangoss-icon2.png" width="100" height="68" style="display: block;
  margin-left: auto;
  margin-right: auto;
  ">
</a>
