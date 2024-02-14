- 👋 Hi, I’m @Douglascosta18170
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ... 

<!---
Douglascosta18170/Douglascosta18170 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->let secretNumber = Math.floor(Math.random() * 10) + 1;
let tries = 3;

function checkGuess() {
    let guess = parseInt(document.getElementById('guessInput').value);
    let message = document.getElementById('message');

    if (guess === secretNumber) {
        message.textContent = 'Congratulations! You guessed the correct number.';
        document.getElementById('guessInput').setAttribute('disabled', 'true');
        document.querySelector('button').setAttribute('disabled', 'true');
    } else {
        tries--;
        if (tries > 0) {
            message.textContent = `Wrong! ${tries} ${tries > 1 ? 'tries' : 'try'} left.`;
        } else {
            message.textContent = `Game over! The correct number was ${secretNumber}.`;
            document.getElementById('guessInput').setAttribute('disabled', 'true');
            document.querySelector('button').setAttribute('disabled', 'true');
        }
    }
}


