# fp-iac
Infrastructure as Code for #teamforeldrepenger

Github workflows avviker noe fra øvrige foreldrepenger repos:
* ved push/merge til main: endringer i kafka-aiven oppsett deployes til dev+prod. Eventuelle sletting av topics må gjøres manuelt vha kubectl etter fjerning fra repo.
* ved endringer av oppsett av fp-kafka-manager: start workflow for deploy av denne manuelt.
