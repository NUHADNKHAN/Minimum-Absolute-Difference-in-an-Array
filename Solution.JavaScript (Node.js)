process.stdin.resume();
process.stdin.setEncoding('ascii');

var input_stdin = "";
var input_stdin_array = "";
var input_currentline = 0;

process.stdin.on('data', function (data) {
    input_stdin += data;
});

process.stdin.on('end', function () {
    input_stdin_array = input_stdin.split("\n");
    main();    
});

function readLine() {
    return input_stdin_array[input_currentline++];
}

/////////////// ignore above this line ////////////////////

function main() {
    var n = parseInt(readLine());
    a = readLine().split(' ');
    a = a.map(Number);
    a.sort();

    const length = a.length;
    let min = Infinity; // Initial minimum absolute value.
    for(let i = 1; i < length; i += 1) {
      const prev = a[i - 1];
      const current = a[i];
      const diff = Math.abs(prev - current);
      min = Math.min(min, diff);
    }

    console.log(min);
}
