🤖 Q&A Chatbot avec LangChain & OpenAI
Un assistant virtuel intelligent basé sur la méthode RAG pour le cours "Introduction to Tableau".

📖 Description du Projet
Ce projet exploite LangChain, un framework avancé pour le développement d'applications basées sur les modèles de langage (LLM). L'objectif principal est de concevoir un chatbot de support client (Q&A) interactif, capable de répondre aux questions des étudiants concernant le cours Introduction to Tableau de Ned Krastev.

Pour atteindre cet objectif, le projet s'appuie sur la technique de Génération Augmentée par la Recherche (RAG), implémentée via le protocole LCEL (LangChain Expression Language). Ce protocole permet de connecter fluidement les composants exécutables de LangChain, où la sortie d'un composant devient l'entrée du suivant.

⚙️ Architecture RAG en 3 Étapes
Le pipeline du chatbot est structuré autour des trois phases fondamentales du RAG :

Indexation (Indexing) : Le transcript du cours est segmenté en petites sections grâce aux séparateurs d'en-têtes Markdown et de tokens de LangChain. Ces sections sont ensuite converties en vecteurs numériques via un modèle d'embedding et stockées dans une base de données vectorielle Chroma.

Recherche (Retrieval) : Un retriever (outil de recherche) interroge la base de données pour extraire les passages du cours les plus pertinents par rapport à la question posée par l'étudiant.

Génération Augmentée (Augmented Generation) : Le modèle de langage fusionne le texte récupéré avec la question initiale grâce à un prompt template. La réponse générée est ensuite traitée par un analyseur de sortie (output parser) pour être renvoyée sous forme de chaîne de caractères claire et contextuelle.

🎯 Compétences Développées
Ce projet met en pratique plusieurs concepts clés de l'ingénierie IA :

Utilisation avancée des Text Splitters de LangChain.

Gestion experte des messages et des Prompt Templates de chat.

Déploiement de LLMs et construction de chaînes LCEL pour la correction de transcriptions.

Génération et stockage d'embeddings dans un Vector Store.

Création de RunnableLambdas à partir de fonctions Python standards.

Conception d'un pipeline complet d'assistant virtuel Q&A.

🛠️ Prérequis et Configuration
Environnement
Il est fortement recommandé de créer un environnement virtuel dédié pour ce projet avec une version de Python >= 3.9 et < 4.0. L'exécution nécessite également un Jupyter Notebook fonctionnel.

⚠️ Note Importante : Ce projet utilise les modèles de langage et d'embedding d'OpenAI. Une clé API OpenAI valide est requise. Assurez-vous de surveiller votre consommation de tokens et les coûts associés.

Installation des Dépendances
Exécutez la commande suivante pour installer les bibliothèques exactes requises et éviter les incompatibilités de syntaxe :

Bash
pip install langchain==0.3.3 langchain-chroma==0.1.4 langchain-community==0.3.2 langchain-openai==0.2.2 pypdf==5.0.1 python-dotenv==1.0.1
(Note : L'installation de langchain v0.3.3 installera automatiquement langchain-core et langchain-text-splitters, qui sont également requis).

Astuce : LangChain étant mis à jour très régulièrement, des différences mineures de syntaxe peuvent exister avec des tutoriels plus anciens. En cas de doute, consultez la documentation officielle de l'API LangChain.

📂 Structure des Fichiers
📄 Introduction_to_Tableau.pdf : Le document source contenant la transcription complète du cours.

📓 LangChain_Project.ipynb : Le squelette du Jupyter Notebook contenant l'architecture de base pour coder le chatbot étape par étape.
