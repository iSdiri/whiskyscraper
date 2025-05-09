Projet scrapy permettant d'extraire de l'information d'un site web. Ici le site visé est https://www.whiskyshop.com/scotch-whisky?item_availability=In+Stock, plateforme vendant du whisky.

Note sur comment faire le projet : 

1. Créer une "shell" pour télécharger la page et l'intérogée : 
    Au terminal :
    scrapy shell
    fetch('https://www.whiskyshop.com/scotch-whisky?item_availability=In+Stock')

2. Retourner sur le site et inspecter l'élément dont on a besoin pour chercher l'information. On peut coller le html de l'info et faire, par exemple, response.css('div.product-item-info') au terminal pour obtenir tout les éléments qui corresponde à ce div. response.css('div.product-item-info').get() permet d'obtenir le html du premier élément de cette liste.

3. Pour conserver un élément dans une variable que l'on peut manipuler (par exemple faire une boucle) :
    Au terminal :
    products = response.css('div.product-item-info')