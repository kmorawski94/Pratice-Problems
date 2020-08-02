# Pratice-Problems
//Leet Translator
//"Leet" or 1337 is a popular alternative alphabet used by internet "hackers".

//Define a function called leetTranslator that take a string of normal characters.

//leetTranslator should return a new string that is the translation of the original string into leet.

//The leet codex is below, along with an array of english letters and an array of the corresponding leet characters. Use the two arrays to create a leetCodex object to use in making the translations.

let letters = [ 'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z' ];
let leetChars = ['@', '8', '(', '|)', '3', 'ph', 'g', '#','l', '_|', '|<', '1', "|'|'|", '/\/', '0', '|D', '(,)', '|2', '5', '+', '|_|', '|/', "|/|/'",'><', 'j', '2'];

// YOUR CODE BELOW
function leetTranslator(normalString) {
  let newString = "";
  let leetCodex = {};
  for (let i = 0; i < letters.length; i++) {
    let normalChar = letters[i];
    let leetChar = leetChars[i];
    leetCodex[normalChar] = leetChar;

    for (let j = 0; j < normalString.length; j++) {
      if (normalString[j] === leetCodex[normalChar]) {
        console.log(normalString[j]);
        newString += leetChar;
      }
    }
  }
  return newString;
}


leetTranslator('apple')
