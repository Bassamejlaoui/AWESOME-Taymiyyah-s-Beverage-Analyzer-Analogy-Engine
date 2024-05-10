# AWESOME Taymiyyah's Beverage Analyzer Analogy Engine
<a href="https://github.com/sindresorhus/awesome"><img src="https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg" alt="Awesome"/></a>

![ghazal](https://github.com/mejbass/AWESOME-Taymiyyah-s-Beverage-Analyzer-Analogy-Engine/assets/130122304/0244e588-9271-43c2-9c24-52fbc443683b)

**This repository hosts a unique analogy engine crafted to ascertain the permissibility of beverages by analyzing their characteristics and cross-referencing them with a database of established drinks. Employing analogical reasoning, the system draws inspiration from Ibn Taymiyyah's critique of Aristotelian logic to arrive at its decisions.**

## Analogical Drink Prohibition Engine

### Components

#### DrinkCase Struct
This structure represents a drink, encapsulating attributes such as name, flavor, color, origin, alcohol content, and its intoxicating and prohibited properties.

#### AttributeWeights Struct
This structure defines the importance (weight) of each attribute. For example, alcohol content might carry more weight than color in determining a drink's prohibition status.

#### AnalogyEngine Class
The core logic of the program resides here. It manages a database of known drinks and utilizes a similarity metric to compare a new drink against the database. This comparison considers attributes and their respective weights. The engine determines if a drink is prohibited by analyzing similar drinks in the database and reaching a decision based on a majority vote.

### Main Functionality

#### Main Function
Users can customize attribute weights, tailoring the analogy engine to different perspectives. The function solicits information about a new drink from the user, including name, flavor, color, origin, and alcohol content. 

### How It Works

1. Users assign weights to various drink attributes, indicating their importance in determining prohibition status.
2. Details about a new drink are provided, with alcohol content above 0.5% deemed intoxicating.
3. The analogy engine compares the new drink to the known drink database, calculating similarity scores based on attributes and user-defined weights.
4. Drinks within 80% similarity of the highest score are considered.
5. If more than half of these similar drinks are prohibited, the new drink is labeled as prohibited; otherwise, it's deemed permissible.
6. The program then displays the prohibition status of the new drink.
