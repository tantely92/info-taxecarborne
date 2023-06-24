<script>
 
  
  import Quizz from '../quizz/Quizz.svelte'; // Remplacez 'TestComponent' par le nom de votre composant Svelte

  let activeSection = null;
  let resultat = null;
  function toggleSection(section) {
    activeSection = section === activeSection ? null : section;
  }
</script>

<main class="bg-gradient-to-r from-blue-200">
  <div class="absolute w-full top-96  mx-auto">
    <div class="bg-gradient-to-r from-blue-200 fixed w-full top-40 py-10 z-20">
    <div class="text-center">
      <h1 class="text-4xl font-bold">Les principales informations</h1>
    </div>
    <div class="flex justify-items-center mt-10">
      <div class="w-2/3 px-4">
        <button class="bg-blue-500 hover:bg-blue-600 transform hover:scale-105 transition-transform duration-200 text-white font-bold py-2 px-4 rounded mb-4" on:click={() => toggleSection(1)}>
          Différents types de tarification carbone
        </button>
      </div>
      <div class="w-2/3 px-4">
        <button class="bg-blue-500 hover:bg-blue-600 transform hover:scale-105 transition-transform duration-200 text-white font-bold py-2 px-4 rounded mb-4" on:click={() => toggleSection(2)}>
          Historique récent en France
        </button>
      </div>
      <div class="w-1/3 px-4">
        <button class="bg-blue-500 hover:bg-blue-600 transform hover:scale-105 transition-transform duration-200 text-white font-bold py-2 px-4 rounded mb-4" on:click={() => toggleSection(3)}>
          Les principaux chiffres en France
        </button>
      </div>
    </div>
    </div>
    {#if activeSection !== null}
      <div class="">
        <div class="w-full">
          <div class="w-full absolute top-5 bg-white rounded-lg shadow-md">
            {#if activeSection === 1}
            
            <div class="">
              <div class= "background1 flex items-center">

                <img src="Mondecarbone.png" alt="Image 1" class="w-1/2 rounded-lg mr-4">
                <div>
                  <h2 id="Introduction" class="text-3xl font-extrabold py-7 text-center mb-2">Introduction </h2>
                  <p class="text-gray-900 font-semibold text-justify ml-4 mr-4 mb-4">Chiffres et panorama global de la tarification carbone 

                    64 initiatives mondiales pour la tarification du carbone, couvrant 22% des émissions de GES. 
                    
                    Plus de 1000 entreprises soumises à des régulations sur le carbone; 700 autres se préparent à suivre. 
                    
                    La CCNUCC de l'ONU (1992) et le Protocole de Kyoto (1997) pionniers pour la réduction des émissions de GES. 
                    
                    Accord de Paris (COP21, 2015): objectif global, limiter le réchauffement à moins de 2°C. Un tournant historique. 
                    
                    La tarification du carbone: un outil clé pour atteindre ces objectifs. 
                    
                    Objectif principal de la taxation carbone: inciter à une économie à faibles émissions de carbone. 
                    
                    Deux méthodes principales: taxes carbone et systèmes d'échange de quotas (marchés carbone). 
                    
                    Les grandes industries souvent incluses dans les marchés carbone; les "petits émetteurs" (voitures, chauffage, etc.) soumis à une taxe carbone. 
                    
                    En France: taxe carbone (2014) et prix carbone en interne pour les entreprises. 
                    
                    Union européenne: système d'échange de quotas d'émission et taxe aux frontières pour les entreprises. </p>
                </div>
              </div>
              <div class="background2 flex items-center">

                
                <div>
                  <h2 id="Marché de quotas carbone entre entreprises cotées"  class="text-3xl font-extrabold py-7 text-center mb-2">Marché de quotas carbone entre entreprises cotées </h2>
                  <p class="text-gray-900 text-justify ml-4 mr-4 mb-4">Marché du carbone: régule les émissions de CO2 en attribuant des quotas aux entreprises. 

                    Les entreprises qui émettent des GES se voient allouer un certain nombre de quotas gratuits pour chaque tonne d'émission autorisée. Si l’entreprise émet plus que son allocation initiale, elle doit acheter des quotas supplémentaires sur le marché. En revanche, si elle émet moins que son allocation, elle peut vendre ses quotas inutilisés.  
                    
                     
                    Créé en 2005; mise en œuvre en plusieurs phases. 
                    
                    Phase 1 (2005-2007): visait les producteurs d'électricité et les entreprises les plus polluantes. 
                    
                    Phase 2 (2008-2012): a inclus d'autres secteurs (industries lourdes, cimenteries, raffineries). 
                    
                    Phase 3 (2013-2020): a instauré des règles plus strictes, a augmenté le taux de réduction des quotas. 
                    
                    Phase 4 (2021-présent): vise des objectifs de réduction des émissions plus ambitieux. </p>
                </div>
                <img src="Marchecarbone.png" alt="Image 1" class="w-1/2 h-full rounded-lg">
              </div>
              <div class="background3 flex items-center">

                <img src="Unioneuropenneecologie.png" alt="Image 1" class="w-1/2 rounded-lg mr-4">
                <div>
                  <h2 id="Taxe aux frontières Européennes pour les entreprises" class="text-3xl font-extrabold py-7 text-center mb-2">Taxe aux frontières Européennes pour les entreprises</h2>
                  <p class="text-gray-900 text-justify mr-4 mb-4">"Mécanisme d'Ajustement Carbone aux Frontières" (MACF) : taxe carbone de l'UE sur certaines importations hors UE. 

                    Objectif : protéger les entreprises européennes contre la concurrence déloyale, éviter le transfert d'émissions de carbone vers des pays aux normes environnementales plus laxistes. 
                    
                    En vigueur à partir du 1er octobre 2023. 
                    
                    Mise en œuvre progressive, commençant avec des secteurs industriels comme la sidérurgie, le ciment, l'aluminium. 
                    
                    Taxe calculée sur l'empreinte carbone des produits importés, appliquée à l'entrée en UE. 
                    
                    Recettes de la taxe utilisées pour financer des projets de réduction des émissions et aider les pays tiers à respecter les normes environnementales. 
                    
                    L'UE vise une tarification uniforme du carbone à l'échelle mondiale, encourageant la réduction des émissions et des pratiques durables. </p>
                </div>
              </div>
              <div class="background4 flex items-center">

                
                <div>
                  <h2 id="Prix du carbone en interne pour les entreprises" class="text-3xl font-extrabold py-7 text-center mb-2">Prix du carbone en interne pour les entreprises</h2>
                  <p class="text-gray-900 font-semibold text-justify ml-4 mr-4 mb-4">Le prix du carbone en interne est une estimation du coût des émissions de CO2 d'une entreprise. 

                    Méthode d'inclusion des coûts environnementaux dans la comptabilité et les décisions d'investissement. 
                    
                    Calculé par tonne de CO2 émise, basé sur les prix des quotas carbone, les coûts de réduction des émissions, les coûts réglementaires ou une combinaison. 
                    
                    Les grandes entreprises françaises fixent leur prix entre 30 et 150 euros par tonne de CO2. 
                    
                    Secteurs comme l'énergie et les matériaux ont des prix plus élevés ; services ont des prix plus bas. 
                    
                    TotalEnergies, Engie, Schneider Electric, L'Oréal utilisent cette méthode pour évaluer leur empreinte carbone. 
                    
                    Mécanisme "100% volontaire" pour anticiper les systèmes de taxation du carbone ou des marchés de quotas de CO2. 
                    
                    Aide à évaluer les coûts et bénéfices de différents projets, aide à la gestion des risques financiers associés à la réglementation future. 
                    
                    Outil clé pour intégrer les coûts environnementaux dans la prise de décision et encourager des comportements plus durables. </p>
                </div>
                <img src="Prixducarboneinterne.png" alt="Image 1" class="w-1/2 h-full rounded-lg">
              </div>
              <div class="background5 flex items-center">

                <img src="Taxecarbone.png" alt="Image 1" class="w-1/2 mr-4 rounded-lg">
                <div>
                  <h2 id="LA Taxe carbone" class="text-3xl font-extrabold py-7 text-center mb-2">LA Taxe carbone</h2>
                  <p class="text-gray-900 font-semibold text-justify ml-4 mr-4 mb-4">"CCE" et "TICPE" sont deux taxes sur les produits énergétiques en France. 

                    "CCE", ou "Contribution Climat Énergie”, est une taxe carbone; "TICPE", ou "Taxe Intérieure de Consommation sur les Produits Énergétiques", est plus large, couvrant tous les produits énergétiques. 
                    
                    La CCE, introduite en 2014, est une composante de la TICPE visant à réduire les émissions de carbone. Son taux augmente annuellement, visant à atteindre 100 euros par tonne de CO2 émise en 2030. 
                    
                    La TICPE s'applique sur les produits pétroliers, le gaz naturel, le charbon et le fioul domestique consommés en France, avec des taux variables selon le type de produit et son usage. 
                    
                    Les recettes de la TICPE financent des politiques pour encourager la réduction de la consommation d'énergie fossile. 
                    
                    La "taxe carbone", ou composante CCE de la TICPE, est conçue pour encourager la réduction de consommation de carburants fossiles, augmentant leurs prix selon leur teneur en carbone. 
                    
                    Le taux actuel de la taxe carbone est de 44,60 €/tonne de CO2. 
                    
                    La taxe carbone s'applique aussi à des secteurs non couverts par la TICPE, comme l'aviation et le transport maritime. Ces secteurs ont mis en place des systèmes de compensation volontaire pour réduire leur empreinte carbone. </p>
                </div>
              </div>
            </div>
            {/if}
            {#if activeSection === 2}
            <div class="flex text-center mt-10">
              <div class="w-1/3 px-4">
                <a href="#Les débuts de la taxe carbone en France" class="hover:text-blue-600 text-gray-600 font-bold py-2 px-4 rounded mb-4">
                  Les débuts de la taxe carbone en France 
                </a>
              </div>
              <div class="w-1/3 px-4">
                <a href="#L'augmentation de la taxe carbone et le déclenchement du mouvement des gilets jaunes" class="hover:text-blue-600 text-gray-600 font-bold py-2 px-4 rounded mb-4">
                  L'augmentation de la taxe carbone et le déclenchement du mouvement des gilets jaunes 
                </a>
              </div>
              
              <div class="w-1/3 px-4">
                <a href="#Vers une nouvelle taxe?" class="hover:text-blue-600 text-gray-600 font-bold py-2 px-4 rounded mb-4">
                  Vers une nouvelle taxe ? 
                </a>
              </div>
              
            </div>


              <div class="flex items-center">
                <img src="ecotaxe.png" alt="Image 2" class="w-16 h-16 mr-4">
                <div>
                  <h2 id="Les débuts de la taxe carbone en France" class="text-xl font-bold mb-2">Les débuts de la taxe carbone en France </h2>
                  <p class="text-gray-700 mb-4">La taxe carbone en France a été introduite lors du Grenelle de l'environnement en 2007, initialement destinée aux poids lourds pour financer l'entretien des infrastructures de transport et le développement des transports en commun. 

                    La Loi de finances pour 2009 a établi cette taxe pour les poids lourds utilisant certaines infrastructures. 
                    
                    L'opposition à la taxe carbone de divers groupes a conduit à des manifestations en Bretagne en 2009, résultant en des exemptions pour certaines routes. 
                    
                    En 2011, un contrat a été signé avec la société Autostrade pour collecter la taxe carbone des poids lourds, ce qui a conduit à la création d'Ecomouv SAS. 
                    
                    En 2012, une garantie de revenus de 230 millions d'euros par an a été fixée pour Autostrade. 
                    
                    La mise en œuvre de la taxe carbone a été confrontée à des retards et des problèmes, avec l'installation des portiques initialement prévue pour juillet 2013, repoussée à octobre 2013, puis au 1er janvier 2014. 
                    
                    Des protestations en Bretagne ont mené à la suspension de l'installation des portiques en novembre 2013. 
                    
                    Ségolène Royal, ministre de l'écologie, a envisagé en 2014 de remplacer la taxe par une vignette pour les camions étrangers, mais ce projet a été suspendu en octobre en raison de protestations. 
                    
                    Le contrat avec Ecomouv a été résilié par l'État en octobre 2014, entraînant un coût final estimé à 957 millions d'euros pour l'État. </p>
                </div>
              </div>
              <div class="flex items-center">
                <img src="gilletsjaunesmanif.png" alt="Image 2" class="w-16 h-16 mr-4">
                <div>
                  <h2 id="L'augmentation de la taxe carbone et le déclenchement du mouvement des gilets jaunes" class="text-xl font-bold mb-2">L'augmentation de la taxe carbone et le déclenchement du mouvement des gilets jaunes  </h2>
                  <p class="text-gray-700 mb-4">La loi de finances 2014 a introduit une taxe carbone, s'appliquant à tous les secteurs économiques, pour aider la France à atteindre ses objectifs de réduction des émissions selon les Accords de Paris 2015. 

                    La taxe carbone, initialement à 7€ par tonne de CO2, a augmenté graduellement jusqu'à 30,5 €/tonne de CO2 en 2017. 
                    
                    Alors que la taxe était initialement peu ressentie durant la baisse des prix du pétrole, son augmentation a été plus visible lors de la hausse des prix du pétrole fin 2018. 
                    
                    En novembre 2018, l'annonce d'une hausse de la taxe carbone a déclenché le mouvement des gilets jaunes, protestant contre la hausse du prix des carburants et soulevant diverses revendications sociales et économiques. 
                    
                    Devant l'ampleur des protestations, le gouvernement a retiré l'augmentation de la taxe carbone pour 2019 et Emmanuel Macron a annoncé plusieurs mesures d'aide, coûtant 10 milliards d'euros. 
                    
                    En janvier 2019, un débat national a été annoncé, menant à la Convention citoyenne pour le climat en octobre, où 150 citoyens ont discuté de mesures climatiques. 
                    
                    En juin 2020, la Convention a soumis 149 propositions, dont l'introduction d'une taxe carbone aux frontières de l'Union européenne pour limiter le réchauffement climatique. </p>
                </div>
              </div>
              <div class="flex items-center">
                <img src="Nouveautetaxe.png" alt="Image 2" class="w-16 h-16 mr-4">
                <div>
                  <h2 id="Vers une nouvelle taxe?" class="text-xl font-bold mb-2">Vers une nouvelle taxe ?</h2>
                  <p class="text-gray-700 mb-4">En avril 2021, l'UE s'accorde sur un objectif de réduction des émissions de gaz à effet de serre de 55 % d'ici 2030 et la neutralité carbone d'ici 2050, fixés dans le paquet climatique "Fit for 55 by 2030". 

                    En juillet 2021, la Commission européenne présente un mécanisme d'ajustement carbone aux frontières de l'UE, introduisant une taxe carbone sur les importations. 
                    
                    Le même mois, la loi Climat et Résilience est adoptée en France, reprenant certaines propositions de la Convention citoyenne pour le climat, dont la réintroduction d'une écotaxe routière laissée au choix des régions. 
                    
                    Les régions Île-de-France, Bourgogne-Franche-Comté et Nouvelle-Aquitaine soutiennent l'écotaxe pour réduire le fret routier et lutter contre le réchauffement climatique. 
                    
                    En décembre 2022, l'UE conclut un accord sur le mécanisme d'ajustement carbone aux frontières, imposant des quotas d'émission de CO2 aux importations de produits polluants et visant à éviter la délocalisation vers des pays aux standards moins exigeants. 
                    
                    Le mécanisme, entré en vigueur le même mois, est suivi d'une période de transition où les importateurs doivent seulement déclarer les émissions liées à la production du produit importé. </p>
                </div>
              </div>
            {/if}
            {#if activeSection === 3}
              <div class="flex items-center">
                <img src="chiffrestaxe.png" alt="Image 3" class="w-16 h-16 mr-4">
                <div>
                  <h2 class="text-xl font-bold mb-2">Chiffres sur la taxe carbone </h2>
                  <p class="text-gray-700 mb-4">Plus de la moitié du prix de l'essence en France (55,6 % pour le diesel, 58,2 % pour l'essence sans plomb 95) est constituée de taxes (analyse de l'UFIP, octobre 2021). 

                    La principale charge fiscale est la TICPE (Taxe Intérieure de Consommation sur les Produits Énergétiques), appelée "taxe carbone", représentant environ 40% du prix à la pompe. 
                    
                    La TVA et la TVA sur la taxe carbone ajoutent environ 16% supplémentaires. 
                    
                    En 2021, l'État récupérait 61,6% des recettes de la taxe carbone, contre 34,9% en 2020. 
                    
                    Depuis 2021, le produit de cette taxe n'est plus spécifiquement affecté au financement de la Transition Énergétique mais va directement dans le budget de l'État. 
                    
                    En 2019, les taxes sur les produits pétroliers ont rapporté 40,5 milliards d'euros à l'État, dont 33,3 milliards provenant de la taxe carbone. 
                    
                    La taxe carbone a augmenté de près de 40% sur le diesel entre 2014 et 2018, impact maintenant plus visible avec la hausse du prix du pétrole. 
                    
                    46 pays ont instauré une taxe carbone, avec des tarifs allant de 1 €/tonne de CO2 en Ukraine à 120 € en Suède. 
                    
                    Le Conseil d'Analyse Économique (CAE) rappelle en 2019 que sans taxe carbone, les objectifs de réduction des émissions de CO2 pour 2030 ne seront pas atteints. </p>
                </div>
              </div>
            {/if}
          </div>
        </div>
      </div>
    {/if}
  </div>
</main>

<style>

p {
  white-space: pre-line;
}

.background1 {
    background-image: linear-gradient(rgba(255, 255, 255, 0.7), rgba(255, 255, 255, 0.7)), url('Mondecarbone.png');
    background-size: cover;
    background-position: center;
  }

  .background2 {
    background-image: linear-gradient(rgba(255, 255, 255, 0.7), rgba(255, 255, 255, 0.7)), url('Marchecarbone.png');
    background-size: cover;
    background-position: center;
  }

  .background3 {
    background-image: linear-gradient(rgba(255, 255, 255, 0.7), rgba(255, 255, 255, 0.7)), url('Unioneuropenneecologie.png');
    background-size: cover;
    background-position: center;
  }

  .background4 {
    background-image: linear-gradient(rgba(255, 255, 255, 0.7), rgba(255, 255, 255, 0.7)), url('Prixducarboneinterne.png');
    background-size: cover;
    background-position: center;
  }

  .background5 {
    background-image: linear-gradient(rgba(255, 255, 255, 0.7), rgba(255, 255, 255, 0.7)), url('Taxecarbone.png');
    background-size: cover;
    background-position: center;
  }

</style>