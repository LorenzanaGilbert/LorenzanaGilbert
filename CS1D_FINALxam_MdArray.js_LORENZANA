// Get names and ages using prompt()  This part is prone to errors if the user doesn't input data correctly.
// Robust error handling would be beneficial in a production environment.

let names = prompt("Enter names separated by commas (e.g., Layla,Julian,Wanwan,Gusion,cecilion):");
let ages = prompt("Enter ages separated by commas (e.g., 24,55,21,6,11):");

//Error Handling for incorrect input
if (!names || !ages) {
    console.error("Please provide both names and ages.");
    return;
}

// Convert strings to arrays
let namesArray = names.split(",").map(name => name.trim());
let agesArray = ages.split(",").map(age => parseInt(age.trim()));

//Error Handling for different array lengths
if (namesArray.length !== agesArray.length) {
    console.error("The number of names and ages must be the same.");
    return;
}

//Error Handling for non-numeric ages
if (agesArray.some(isNaN)) {
    console.error("All ages must be numeric values.");
    return;
}

// Restructure the array
let restructuredArray = [];
for (let i = 0; i < namesArray.length; i++) {
  restructuredArray.push([namesArray[i], agesArray[i]]);
}

// Log the restructured array
console.log("Restructured array (name, age):");
restructuredArray.forEach(item => {
  console.log(item); // Output: [name, age] per line.
});
