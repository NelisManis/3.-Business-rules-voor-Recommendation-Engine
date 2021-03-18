# 3.-Business-rules-voor-Recommendation-Engine

Dit is de opdracht Buisness rules voor Recommendation Engine van het vak SP van Niels van der Smeede.
Voor deze opdracht moeten we de zogenaamde Buisness rules implementeren in een systeem die we kunnen toepassen op de data.
We moeten lijsten met product ids genereren, waardoor het makkelijk wordt om vanuit de frontend relevanten producten op te vragen als recommendation.
Voor deze opdracht moeten we alleen logische regels opstellen die we kunnen toepassen op de data.

Mogelijke regels:
  Content filtering:
    Product met herhaalaankoop op True en al eerder gekocht, krijgt voorang.
    Product met recommandeble op True en category, sub-category en sub-sub-category
      hetzelfde als een eerdergekocht procuct met herhaalaankoop op True, krijgt voorang.

  Collaborative filtering:
    Twee profilen waarbij minimaal 25% van de producten uit vieuwed_before dezelfde category, sub-category en sub-sub-category hebben,
      heeft een ander product van profiel 1 met een ander category, sub-category en sub-sub-category voorang bij profiel 2,
      zolang recommandeble op true staat van het andere product.
    Twee profilen waarbij minimaal 25% van de producten uit previously_recommended dezelfde category, sub-category en sub-sub-category hebben,
      heeft een ander product van profiel 1 met een ander category, sub-category en sub-sub-category voorang bij profiel 2,
      zolang recommandeble op true staat van het andere product.
