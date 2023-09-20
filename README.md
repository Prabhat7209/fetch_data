Store the data obtained in the  file and use that file in other program.

1.Import the fs module. This module provides functions for working with files.

2.Write the data to a file using the fs.writeFile() function. This function takes the path to the file and the data to write as parameters.

3.Read the data from the file using the fs.readFile() function. This function takes the path to the file as a parameter and returns the data in the file as a buffer.

4.Convert the buffer to a string using the toString() method.

5.Use the data in your program.






Node.js Code:
const fs = require('fs').promises; async function readFile(filePath) {
try {
const data = await fs.readFile(filePath); // Corrected file path usage console.log(data.toString());
const data1 = data.toString();
await fs.writeFile('Z:\\SUMEET\\Sem_3\\backend\\experiment_2.html', data1); // Added 'await' here console.log('File has been written successfully.'); // Added a success message
} catch (error) {
console.error(`Got an error trying to read the file: ${error.message}`); // Fixed template literal
}
}

readFile('Z:\\SUMEET\\Sem_3\\backend\\show&hide.html');
