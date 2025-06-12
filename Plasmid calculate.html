# Lab
About lab daily work
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Multi-Plasmid Dilution Calculator</title>
  <style>
    body { font-family: Arial, sans-serif; padding: 20px; background: #f9f9f9; }
    h2 { color: #333; }
    .input-group { margin-bottom: 10px; }
    label { display: block; margin-bottom: 5px; }
    input, select { width: 100%; padding: 8px; }
    button { padding: 10px 20px; margin-top: 10px; cursor: pointer; }
    .result { margin-top: 20px; font-weight: bold; }
    .plasmid-entry { border: 1px solid #ccc; padding: 10px; margin-bottom: 10px; background: #fff; }
  </style>
</head>
<body>
  <h2>Multi-Plasmid Dilution Calculator</h2>

  <div id="plasmidContainer"></div>
  <button onclick="addPlasmidEntry()">Add Plasmid</button>

  <div class="input-group">
    <label for="totalVolume">Total Final Volume:</label>
    <input type="number" id="totalVolume" step="any">
    <select id="totalVolumeUnit">
      <option value="1">μL</option>
      <option value="1000">mL</option>
    </select>
  </div>

  <button onclick="calculateMixture()">Calculate</button>

  <div class="result" id="result"></div>

  <script>
    let plasmidCount = 0;

    function addPlasmidEntry() {
      const container = document.getElementById('plasmidContainer');
      const div = document.createElement('div');
      div.classList.add('plasmid-entry');
      div.innerHTML = `
        <div class="input-group">
          <label>Plasmid Name:</label>
          <input type="text" id="name${plasmidCount}">
        </div>
        <div class="input-group">
          <label>Stock Concentration:</label>
          <input type="number" id="stock${plasmidCount}" step="any">
          <select id="stockUnit${plasmidCount}">
            <option value="1000000">mg/μL</option>
            <option value="1000">μg/μL</option>
            <option value="1">ng/μL</option>
          </select>
        </div>
        <div class="input-group">
          <label>Final Concentration:</label>
          <input type="number" id="final${plasmidCount}" step="any">
          <select id="finalUnit${plasmidCount}">
            <option value="1000000">mg/μL</option>
            <option value="1000">μg/μL</option>
            <option value="1">ng/μL</option>
          </select>
        </div>
      `;
      container.appendChild(div);
      plasmidCount++;
    }

    function calculateMixture() {
      const totalVolume = parseFloat(document.getElementById('totalVolume').value);
      const volumeUnit = parseFloat(document.getElementById('totalVolumeUnit').value);
      const realTotalVolume = totalVolume * volumeUnit;

      let totalStockVolume = 0;
      let results = '<h3>Mixing Instructions:</h3><ul>';

      for (let i = 0; i < plasmidCount; i++) {
        const name = document.getElementById(`name${i}`).value || `Plasmid ${i+1}`;
        const stockConc = parseFloat(document.getElementById(`stock${i}`).value);
        const stockFactor = parseFloat(document.getElementById(`stockUnit${i}`).value);
        const finalConc = parseFloat(document.getElementById(`final${i}`).value);
        const finalFactor = parseFloat(document.getElementById(`finalUnit${i}`).value);

        if (isNaN(stockConc) || isNaN(finalConc) || stockConc === 0) {
          document.getElementById('result').innerHTML = 'Please enter valid values for all plasmids.';
          return;
        }

        const stockConcNg = stockConc * stockFactor;
        const finalConcNg = finalConc * finalFactor;
        const requiredMass = finalConcNg * realTotalVolume; // in ng
        const stockVolume = requiredMass / stockConcNg;
        totalStockVolume += stockVolume;
        results += `<li>${name}: <strong>${stockVolume.toFixed(2)} μL</strong></li>`;
      }

      const waterVolume = realTotalVolume - totalStockVolume;
      if (waterVolume < 0) {
        document.getElementById('result').innerHTML = 'Total plasmid volume exceeds final volume. Please adjust concentrations.';
      } else {
        results += `<li>Water: <strong>${waterVolume.toFixed(2)} μL</strong></li></ul>`;
        document.getElementById('result').innerHTML = results;
      }
    }
  </script>
</body>
</html>
