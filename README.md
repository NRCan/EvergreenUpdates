# 🌲 EvergreenUpdates

A simple desktop tool enabled by AI that scans websites for news articles and compiles them into a CSV. Built for policy teams who need to monitor large numbers of stakeholder sites without manual checking.

## What It Does

Enter a list of URLs and the tool will scan each one for news articles, collecting the title, link, date published, date retrieved, and source URL into a single CSV file.

## Requirements

To use this tool you will need:
- A **Google API key** (see [Getting an API Key](#getting-an-api-key) below)
- A **PEM certificate file** (for secure connections to your organization's network, see [Contact](#contact) for support if you work for NRCan)
- Python 3.10 or newer (only for [Getting Started, Option 2](#option-2-run-the-python-script))

## Getting Started

### Option 1: Run the Executable (Recommended)
1. Go to the [EvergreenUpdates Releases](../../releases) page
2. Select the latest release
3. Scroll to the bottom of the release page and expand the Assets section
4. Under Assets, click EvergreenUpdates.exe to download the application. (Windows security notice: you will need to indicate that you trust this download)
5. Enter your Google API key, the path to your `.pem` certificate, and your list of URLs (one per line)
6. Click Run - your CSV will be saved to the same folder as the executable

### Option 2: Run the Python Script
1. Clone this repository
2. Create and activate a virtual environment:

   Windows
   ```bash
   python -m venv .venv
   .venv\Scripts\Activate.ps1
   ```
   macOS / Linux
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```
3. Install dependencies
   ```bash
   pip install -r requirements.txt
   ```
4. Run the script:
   ```bash
   python src/scraper.py
   ```

## Getting an API Key

This tool uses the Google API for article discovery. To get a free API key:
1. Go to [https://aistudio.google.com/api-keys](https://aistudio.google.com/api-keys)
2. Sign in with your Google account
3. Click **Create API key**
4. Copy the key and paste it into the app when prompted

## Output

The tool produces a CSV file named **`news_results.csv`** by default — you can change this in the UI before running. It contains the following columns:

| Column | Description |
|---|---|
| title | Article headline |
| url | URL to the article |
| published_date | Date the article was published |
| retrieved_on | Date the tool found the article |
| source_url | The website URL you provided |

As with all AI generated content, please be aware that the results may be inaccurate. 

## Notes
- URLs should be entered one per line in the text box
- The tool works best with news and press release pages rather than homepages
- Your API key and certificate path are never saved or transmitted

## Contact
Valerie Gies @ valerie.gies@nrcan-rncan.gc.ca

***

# 🌲 EvergreenUpdates
Un outil de bureau simple, propulsé par l'IA, qui analyse des sites web à la recherche d'articles d'actualité et les compile dans un fichier CSV. Conçu pour les équipes de politiques qui doivent surveiller un grand nombre de sites de parties prenantes sans vérification manuelle.

## Ce que fait l'outil
Entrez une liste d'URL et l'outil analysera chacune d'elles à la recherche d'articles d'actualité, en recueillant le titre, le lien, la date de publication, la date de récupération et l'URL source dans un seul fichier CSV.

## Prérequis
Pour utiliser cet outil, vous aurez besoin de :
- Une **clé API Google** (voir [Obtenir une clé API](#obtenir-une-clé-api) ci-dessous)
- Un **fichier de certificat PEM** (pour les connexions sécurisées au réseau de votre organisation; voir [Contact](#contact) pour obtenir de l'aide si vous travaillez pour RNCan)
- Python 3.10 ou plus récent (uniquement pour l'[Option 2 de mise en route](#option-2--exécuter-le-script-python))

## Mise en route
### Option 1 : Exécuter le fichier exécutable (recommandé)
1. Accédez à la page des [versions d'EvergreenUpdates](../../releases)
2. Sélectionnez la dernière version
3. Faites défiler jusqu'au bas de la page de la version et développez la section Assets
4. Sous Assets, cliquez sur EvergreenUpdates.exe pour télécharger l'application. (Avis de sécurité Windows : vous devrez indiquer que vous faites confiance à ce téléchargement)
5. Entrez votre clé API Google, le chemin d'accès à votre certificat `.pem`, ainsi que votre liste d'URL (une par ligne)
6. Cliquez sur Exécuter — votre fichier CSV sera enregistré dans le même dossier que le fichier exécutable

### Option 2 : Exécuter le script Python
1. Clonez ce dépôt
2. Créez et activez un environnement virtuel :
   
Windows
```bash
   python -m venv .venv
   .venv\Scripts\Activate.ps1
```
macOS / Linux
```bash
   python -m venv .venv
   source .venv/bin/activate
```
3. Installez les dépendances
```bash
   pip install -r requirements.txt
```
4. Exécutez le script :
```bash
   python src/scraper.py
```

## Obtenir une clé API
Cet outil utilise l'API Google pour la découverte d'articles. Pour obtenir une clé API gratuite :
1. Rendez-vous sur [https://aistudio.google.com/api-keys](https://aistudio.google.com/api-keys)
2. Connectez-vous avec votre compte Google
3. Cliquez sur **Créer une clé API**
4. Copiez la clé et collez-la dans l'application lorsque vous y êtes invité

## Résultat
L'outil produit par défaut un fichier CSV nommé **`news_results.csv`** — vous pouvez modifier ce nom dans l'interface avant l'exécution. Il contient les colonnes suivantes :

| Colonne | Description |
|---|---|
| title | Titre de l'article |
| url | URL de l'article |
| published_date | Date de publication de l'article |
| retrieved_on | Date à laquelle l'outil a trouvé l'article |
| source_url | L'URL du site web que vous avez fournie |

Comme pour tout contenu généré par l'IA, veuillez noter que les résultats peuvent être inexacts.

## Remarques
- Les URL doivent être saisies une par ligne dans la zone de texte
- L'outil fonctionne mieux avec les pages d'actualités et de communiqués de presse qu'avec les pages d'accueil
- Votre clé API et le chemin d'accès à votre certificat ne sont jamais enregistrés ni transmis

## Contact
Valerie Gies @ valerie.gies@nrcan-rncan.gc.ca
