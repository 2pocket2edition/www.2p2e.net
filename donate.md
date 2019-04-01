---
layout: default
---

Donate to keep the server running. Money from donations will go towards paying the power bill as well as things like domain name renewal.

Additionally, since I no longer give a single crap about this pile of shit server, it also goes towards motivating me not to delete it.



<p id="addresses">Loading...</p>



<script>
    fetch("https://gist.githubusercontent.com/DaMatrix/8b7ff92fcc7e49c0f511a8ed207d8e92/raw/www.daporkchop.net-donate-addresses.json").then(response => {
        return response.json();
    }).then(data => {
        var html = "";
        for (var i = 0; i < data.length; i++)   {
            var curr = data[i];
            html += "<a href=\"" + curr.url + "\">" + curr.symbol + "</a>: <code class=\"highlighter-rouge\">" + curr.address + "</code><br>";
        }
        document.getElementById("addresses").innerHTML = html;
    });
</script>
