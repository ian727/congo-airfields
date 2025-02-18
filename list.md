---
layout: page
title: "List of Airports"
show_title: false
---

[en français](list_fr.md)

## List of Airports in the Democratic Republic of the Congo

Below, you will find a comprehensive list of airports and airfields in the DRC. Implementing every bit of information is a lot of work, so this page will continuously be updated. So far, the following airports are included:

## Browse Airports:

*Click on the columns to sort the table respectively!*

<table id="airportTable">
  <thead>
    <tr>
      <th onclick="sortTable(0)">Name</th>
      <th onclick="sortTable(1)">ICAO Code</th>
      <th onclick="sortTable(2)">IATA Code</th>
      <th onclick="sortTable(3)">Province</th>
      <th onclick="sortTable(4)">Status</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="airports/bikorofzbc/bikoro.html">Bikoro Airport</a></td>
      <td>FZBC</td>
      <td>-</td>
      <td>Équateur</td>
      <td>Unknown</td>
    </tr>
    <tr>
      <td><a href="airports/bokoro/bokoro.html">Bokoro Airport</a></td>
      <td>-</td>
      <td>-</td>
      <td>Mai-Ndombe</td>
      <td>Active</td>
    </tr>
    <tr>
      <td><a href="airports/bomafzaj/boma.html">Boma Airport (old)</a></td>
      <td>FZAJ</td>
      <td>BOA</td>
      <td>Kongo Central</td>
      <td>Redeveloped</td>
    </tr>
    <tr>
      <td><a href="airports/bomafzaj/boma.html">Boma Lukandu Airport</a></td>
      <td>-</td>
      <td>-</td>
      <td>Kongo Central</td>
      <td>Active</td>
    </tr>
    <tr>
      <td><a href="airports/zongofzad/zongo.html">Celo-Zongo Airport</a></td>
      <td>FZAD</td>
      <td>-</td>
      <td>Kongo Central</td>
      <td>Active</td>
    </tr>
    <tr>
      <td><a href="airports/inkisifzas/inkisi.html">Inkisi Airport</a></td>
      <td>FZAS</td>
      <td>-</td>
      <td>Kongo Central</td>
      <td>Abandoned</td>
    </tr>
    <tr>
      <td><a href="airports/kimpokofzad/kimpoko.html">Kimpoko Airport</a></td>
      <td>FZAD</td>
      <td>-</td>
      <td>Kinshasa</td>
      <td>Redeveloped</td>
    </tr>
    <tr>
      <td><a href="airports/binzafzak/binza.html">Kinshasa Binza Airport</a></td>
      <td>FZAK</td>
      <td>-</td>
      <td>Kongo Central</td>
      <td>Unknown</td>
    </tr>
    <tr>
      <td><a href="airports/ndjilifzaa/ndjili.html">Kinshasa N'Djili Airport</a></td>
      <td>FZAA</td>
      <td>FIH</td>
      <td>Kinshasa</td>
      <td>Active</td>
    </tr>
    <tr>
      <td><a href="airports/ndolofzab/ndolo.html">Kinshasa N'Dolo Airport</a></td>
      <td>FZAB</td>
      <td>NLO</td>
      <td>Kinshasa</td>
      <td>Active</td>
    </tr>
    <tr>
      <td><a href="airports/kitonabasefzai/kitona.html">Kitona Base Airport</a></td>
      <td>FZAI</td>
      <td>-</td>
      <td>Kongo Central</td>
      <td>Active</td>
    </tr>
    <tr>
      <td><a href="airports/kondefzau/konde.html">Konde Airport</a></td>
      <td>FZAU</td>
      <td>-</td>
      <td>Kongo Central</td>
      <td>Unknown</td>
    </tr>
    <tr>
      <td><a href="airports/luozifzal/luozi.html">Luozi Airport</a></td>
      <td>FZAL</td>
      <td>-</td>
      <td>Kongo Central</td>
      <td>Intermittent</td>
    </tr>
    <tr>
      <td><a href="airports/malukufzac/maluku.html">Maluku Airport</a></td>
      <td>FZAC</td>
      <td>-</td>
      <td>Kinshasa</td>
      <td>Active</td>
    </tr>
    <tr>
      <td><a href="airports/matadifzam/matadi.html">Matadi Airport</a></td>
      <td>FZAM</td>
      <td>MAT</td>
      <td>Kongo Central</td>
      <td>Active</td>
    </tr>
    <tr>
      <td><a href="airports/muandafzag/muanda.html">Muanda Airport</a></td>
      <td>FZAG</td>
      <td>MNB</td>
      <td>Kongo Central</td>
      <td>Active</td>
    </tr>
    <tr>
      <td><a href="airports/nsangifzaf/nsangi.html">Nsangi Airport</a></td>
      <td>FZAF</td>
      <td>-</td>
      <td>Kongo Central</td>
      <td>Unknown</td>
    </tr>
    <tr>
      <td><a href="airports/tshelafzah/tshela.html">Tshela Airport</a></td>
      <td>FZAH</td>
      <td>-</td>
      <td>Kongo Central</td>
      <td>Abandoned</td>
    </tr>
  </tbody>
</table>

[← Back to Homepage](index.md)

<script>
function sortTable(columnIndex) {
  let table = document.getElementById("airportTable");
  let rows = Array.from(table.getElementsByTagName("tr")).slice(1);
  let sortedRows = rows.sort((a, b) => {
    let aValue = a.cells[columnIndex].innerText.trim();
    let bValue = b.cells[columnIndex].innerText.trim();

    if (!isNaN(aValue) && !isNaN(bValue)) {
      return parseFloat(aValue) - parseFloat(bValue);
    }

    return aValue.localeCompare(bValue);
  });

  let tbody = table.getElementsByTagName("tbody")[0];
  tbody.innerHTML = "";
  sortedRows.forEach(row => tbody.appendChild(row));
}
</script>
