---
layout: page
title: "List of Airports"
show_title: false
---

[en français](list_fr.md)

## List of Airports in the Democratic Republic of the Congo

Below, you will find a comprehensive list of airports and airfields in the DRC. Implementing every bit of information is a lot of work, so this page will continuously be updated. So far, the following airports are included:

## Browse Airports:

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
      <td><a href="airports/bikorofzbc/bikoro.md">Bikoro Airport</a></td>
      <td>FZBC</td>
      <td>-</td>
      <td>Équateur</td>
      <td>Active</td>
    </tr>
    <tr>
      <td><a href="airports/bokoro/bokoro.md">Bokoro Airport</a></td>
      <td>-</td>
      <td>-</td>
      <td>Mai-Ndombe</td>
      <td>Unknown</td>
    </tr>
    <tr>
      <td><a href="airports/bomafzaj/boma.md">Boma Airport (old)</a></td>
      <td>FZAJ</td>
      <td>-</td>
      <td>Kongo-Central</td>
      <td>Closed</td>
    </tr>
    <tr>
      <td><a href="airports/bomafzaj/boma.md">Boma Lukandu Airport</a></td>
      <td>-</td>
      <td>-</td>
      <td>Kongo-Central</td>
      <td>Unknown</td>
    </tr>
    <tr>
      <td><a href="airports/zongofzad/zongo.md">Celo-Zongo Airport</a></td>
      <td>FZAD</td>
      <td>-</td>
      <td>Équateur</td>
      <td>Active</td>
    </tr>
    <!-- Add more airports here -->
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
