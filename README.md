// json2html.js

export default function json2html(data) {
  // Define the headers for the table
  const headers = ["Name", "Age", "Gender"];
  
  // Start building the HTML string with the table and user data attribute
  let html = `<table data-user="bpratapsingh281@gmail.com">`;

  // Add the table headers
  html += `<thead><tr>${headers.map(header => `<th>${header}</th>`).join('')}</tr></thead>`;

  // Add table rows from the data array
  html += `<tbody>`;
  data.forEach(row => {
    html += `<tr>${headers.map(header => `<td>${row[header] || ''}</td>`).join('')}</tr>`;
  });
  html += `</tbody></table>`;

  return html;
}
