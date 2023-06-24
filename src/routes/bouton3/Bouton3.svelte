<script>
    /**
   * @type {number | null}
   */
    let activeSection = null;
  
    /**
   * @param {number | null} section
   */
    function toggleSection(section) {
      activeSection = section === activeSection ? null : section;
    }
  </script>
  
  <main class="bg-blue-200 py-10">
    <div class="container mx-auto px-4">
      <div class="text-center">
        <h1 class="text-4xl font-bold mb-4">Maintenant, co-construisons!</h1>
        <p class="text-lg text-gray-700">Et ... inspirez nous! </p>
      </div>
      
      <div class="flex justify-center mt-10">
        <div class="w-1/3 px-4">
          <button class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mb-4" on:click={() => toggleSection(1)}>
            Les principaux axes de réflexion
          </button>
        </div>
        <div class="w-1/3 px-4">
          <button class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mb-4" on:click={() => toggleSection(2)}>
            Les pistes pour l'entreprise
          </button>
        </div>
        <div class="w-1/3 px-4">
            <button class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mb-4" on:click={() => toggleSection(3)}>
              ... vos pistes! 
            </button>
          </div>
        
      </div>
      {#if activeSection !== null}
      <div class="flex justify-center mt-4">
        <div class="w-full">
          <div class="bg-white rounded-lg shadow-md p-6">
            {#if activeSection === 1}

            <div class="flex justify-center mt-10">
                <div class="w-1/3 px-4">
                  <a href="#redistribution" class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mb-4">
                    redistribution
                  </a>
                </div>
                <div class="w-1/3 px-4">
                  <a href="#emploi et entreprise" class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mb-4">
                    emploi et entreprise
                  </a>
                </div>
                <div class="w-1/3 px-4">
                  <a href="#ISF climatique" class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mb-4">
                    ISF climatique
                  </a>
                </div>
                <div class="w-1/3 px-4">
                  <a href="#particularité des ménages" class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mb-4">
                    particularité des ménages
                  </a>
                </div>
                <div class="w-1/3 px-4">
                    <a href="#flexibilité" class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mb-4">
                        flexibilité
                    </a>
                  </div>
                  <div class="w-1/3 px-4">
                    <a href="#prix du carbone" class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mb-4">
                        prix du carbone
                    </a>
                  </div>
                  <div class="w-1/3 px-4">
                    <a href="#autres formes de tarification" class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mb-4">
                        autres formes de tarification
                    </a>
                  </div>
                  <div class="w-1/3 px-4">
                    <a href="#méthane et kérozène" class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mb-4">
                        méthane et kérozène
                    </a>
                  </div>
            </div>


            <div class="flex items-center">
              <img src="recettesfiscales.png" alt="Image 1" class="w-16 h-16 mr-4">
              <div>
                <h2 id="redistribution" class="text-xl font-bold mb-2">Changement de la base d’imposition et redistribution des recettes</h2>
                <p class="text-gray-700 mb-4">Exigence de transparence : Terra Nova et I4CE insistent sur le besoin d'une transparence totale concernant l'utilisation des recettes générées par une éventuelle augmentation de la taxe carbone. Ces recettes doivent être traçables pour assurer qu'elles sont utilisées pour les objectifs déclarés. 

                    Justice sociale : Une importance accrue doit être accordée à l'aide aux ménages les plus modestes, potentiellement les plus touchés par la taxe carbone. En parallèle, il est recommandé d'augmenter la taxation des secteurs actuellement exemptés mais qui sont fortement polluants. 
                    
                    Investissement pour la transition écologique : Les recettes de la taxe carbone devraient être investies dans la promotion de l'efficacité énergétique, la mobilité propre et d'autres initiatives visant à accélérer la transition écologique. 
                    
                    Utilisation exclusive des recettes de la taxe carbone : Ces fonds devraient être strictement dédiés à la mise en œuvre des deux objectifs précédents - soutien aux ménages modestes et investissement dans la transition écologique. 
                    
                    Compensation fiscale : Si une augmentation de la taxe carbone est envisagée, elle devrait être compensée par une baisse équivalente d'un ou de plusieurs autres prélèvements fiscaux. 
                    
                    Approche multidimensionnelle : Terra Nova et I4CE soutiennent que la taxe carbone ne peut pas être envisagée isolément, elle doit être combinée avec d'autres mesures, notamment la réglementation, la taxation de secteurs spécifiques, les subventions et la création de marchés de «droits à polluer» </p>
              </div>
            </div>
            <div class="flex items-center">
                <img src="emploi.png" alt="Image 1" class="w-16 h-16 mr-4">
                <div>
                  <h2 id="emploi et entreprise" class="text-xl font-bold mb-2">Axe emploi et entreprise </h2>
                  <p class="text-gray-700 mb-4">Absence d'effet sur la création nette d'emplois : Selon une étude de l'OCDE, la variation des prix de l'énergie et la taxe carbone n'auraient pas d'impact direct sur la création totale d'emplois, bien qu'ils puissent entraîner des déplacements d'emplois des entreprises intensives en énergie vers celles moins intensives. 

                    Impacts sur les employés : Ces redéploiements d'emplois pourraient entraîner une diminution des revenus, nécessiter des adaptations à la vie quotidienne en cas de changement de zone géographique et avoir un impact sur la santé mentale des employés licenciés. 
                    
                    Recommandation de politiques complémentaires sur le marché du travail : Pour atténuer ces effets, l'étude recommande la mise en place de politiques d'accompagnement sur le marché du travail. Cela peut inclure la formation professionnelle et les allocations chômage pour soutenir les travailleurs en transition entre les industries. 
                    
                    Redistribution des revenus de la taxe carbone : Les économistes Thomas Piketty et Jean Tirole proposent d'utiliser les revenus générés par la taxe carbone pour réduire les inégalités. Cela pourrait être fait en modifiant les taux d'imposition sur le revenu pour favoriser les plus pauvres. 
                    
                    Mise en place d'un revenu de base universel : Une autre proposition consiste à mettre en place un revenu de base universel, soit un montant d'argent inconditionnel donné à tous les citoyens. Cela pourrait aider à compenser l'impact de la taxe carbone sur les ménages à faible revenu. 
                    
                    Approche centrée sur le bien-être des travailleurs : Il est recommandé de prendre en compte l'impact de la taxe carbone sur les travailleurs et de mettre en place des mesures pour minimiser les effets négatifs, comme l'offre de formations et de soutiens pour les travailleurs déplacés par la transition vers des industries moins énergivores. 
                    
                     </p>
                </div>
              </div>
            <div class="flex items-center">
                <img src="Livrearbre.png" alt="Image 1" class="w-16 h-16 mr-4">
                <div>
                  <h2 id="ISF climatique" class="text-xl font-bold mb-2">Axe ISF climatique </h2>
                  <p class="text-gray-700 mb-4">Introduction de l'ISF climatique : Proposé par Greenpeace et OXFAM, l'ISF climatique vise à taxer les grandes fortunes en fonction de leur contribution au changement climatique. Les émissions de gaz à effet de serre générées par les entreprises détenues par les personnes fortunées seraient prises en compte. 

                    Critique de la taxe carbone actuelle : Ces organisations soulignent que la taxe carbone actuelle peut être socialement injuste car elle pèse davantage sur les ménages modestes, tout en laissant les grandes entreprises polluantes largement impunies. 
                    
                    Études sur l'empreinte carbone : Selon les données de l'Insee et du cabinet Carbone 4, utilisées par Greenpeace, le patrimoine financier des 10% les plus riches est associé à une empreinte carbone bien supérieure à celle des 10% les plus pauvres. Les partisans de l'ISF climatique soutiennent donc qu'il pourrait aider à réduire les émissions en taxant les plus gros pollueurs. 
                    
                    Préconisations de Greenpeace : L'ONG recommande de rétablir l'ISF comme il était en 2017 et de l'augmenter, tout en introduisant une composante carbone, basée sur l'empreinte carbone moyenne des placements financiers des ménages concernés. 
                    
                    Estimations des recettes : Si cette mesure était appliquée, elle pourrait générer environ 4,3 milliards d'euros de recettes supplémentaires pour l'État, selon Greenpeace France. 
                    
                    Analyse d'Oxfam : Selon une étude d'Oxfam France, les milliardaires français émettent en moyenne 13 fois plus de gaz à effet de serre que le citoyen moyen. L'ONG appelle à des mesures d'urgence pour réduire les émissions des plus riches, y compris une taxation progressive. </p>
                </div>
            </div>
            <div class="flex items-center">
                <img src="menages.png" alt="Image 1" class="w-16 h-16 mr-4">
                <div>
                  <h2 id="particularité des ménages" class="text-xl font-bold mb-2">Axe particularité des ménages </h2>
                  <p class="text-gray-700 mb-4">Création d'un revenu climatique : Plusieurs ONG ont proposé de créer un "revenu climatique" pour compenser l'impact disproportionné de la taxe carbone sur les ménages à faible revenu. Financé par les recettes existantes de la taxe carbone et les économies réalisées grâce à la réduction des exonérations fiscales sur les produits énergétiques, ce revenu viserait à atténuer l'impact des augmentations des prix de l'énergie sur les ménages les plus vulnérables. 

                    Application du principe de pollueur-payeur : Ce principe, consistant à faire payer aux pollueurs le coût de leur pollution, est un autre pilier de ces propositions. Il viserait à garantir que les principaux émetteurs de gaz à effet de serre contribuent de manière significative à la lutte contre le changement climatique. 
                    
                    Financement de la transition écologique : Les recettes générées par la taxe carbone et le revenu climatique seraient utilisées pour financer des projets de transition écologique, contribuant ainsi à une économie plus verte. 
                    
                    Introduction d'une contribution climat solidaire : Les 60% des ménages les plus modestes recevraient le revenu de l'augmentation de la taxe carbone, contribuant à la neutralité de la hausse des taxes pour 50% des ménages. 
                    
                    Mise en place d'un outil de calcul de la taxe carbone équitable : Le Réseau Action Climat, en collaboration avec le Secours Catholique et OXFAM, a proposé un calculateur permettant aux individus de déterminer leur contribution à la taxe carbone en fonction de leur situation personnelle. Cet outil vise à garantir que les taxes carbone sont réparties de manière équitable, en tenant compte du niveau de revenu des individus. 
                    
                    Adaptation des aides en fonction des contraintes géographiques et de revenus : Les aides, comme le chèque énergie, pourraient être modulées en fonction des revenus, mais aussi en fonction de la distance qui sépare le domicile d'une gare ou d'une ligne de bus, de manière à cibler plus précisément les ménages les plus vulnérables.  </p>
                </div>
            </div>
            <div class="flex items-center">
                <img src="flexibilite.png" alt="Image 1" class="w-16 h-16 mr-4">
                <div>
                  <h2 id="flexibilité" class="text-xl font-bold mb-2">Plus de flexibilité pour la taxe carbone  </h2>
                  <p class="text-gray-700 mb-4">Taxation plus élevée pour ceux ayant accès à des alternatives : Thomas Porcher propose une taxe carbone plus élevée pour ceux qui, bien qu'ayant accès à des modes de transport moins polluants, choisissent néanmoins des véhicules à forte cylindrée. 

                    Taxation accrue des ultrariches : Christian Gollier propose une taxe carbone plus élevée pour les individus et les activités les plus riches, comme les jets privés. Cela enverrait un signal fort sur le coût environnemental de ces choix de vie. 
                    
                    Taxation progressive des émissions : Thomas Piketty propose une approche progressive, avec aucune taxe sur les premières tonnes d'émissions de CO2, puis une augmentation progressive jusqu'à un certain plafond. 
                    
                    Amortissement des chocs du prix du pétrole et du gaz : Wilfried Sand-Zantman propose de moduler la taxe carbone en fonction des variations des prix du pétrole et du gaz. Si ces prix augmentent fortement, la taxe carbone pourrait être réduite pour éviter de trop peser sur le budget des ménages. 
                    
                    Développement d'alternatives écologiques : Pour que la taxe carbone soit efficace, il est indispensable d'offrir des alternatives écologiques. Cela pourrait passer par le développement des transports en commun et du covoiturage, notamment en zone rurale, et par l'augmentation des subventions pour les énergies renouvelables et les modes de transport doux (vélo, etc.). 
                    
                    Soutien financier pour l'adoption d'alternatives écologiques : Il serait également nécessaire de mettre en place des mesures de soutien financier pour encourager l'adoption de ces alternatives, en particulier pour les ménages à revenus modestes. Cela pourrait prendre la forme de subventions, de prêts à taux zéro, ou de crédits d'impôt pour l'achat de véhicules moins polluants ou la rénovation énergétique de l'habitat. </p>
                </div>
            </div>
            <div class="flex items-center">
                <img src="Marchecarbone.png" alt="Image 1" class="w-16 h-16 mr-4">
                <div>
                  <h2 id="prix du carbone" class="text-xl font-bold mb-2"> 
                    Trouver le prix idéal du carbone  </h2>
                  <p class="text-gray-700 mb-4">Disparités dans les modèles de tarification : Les travaux de différents économistes sur le prix du carbone, à commencer par William Nordhaus, ont conduit à diverses propositions allant de 50 € à 250 € par tonne de CO2, reflétant l'éventail des idéologies et des hypothèses derrière ces modèles. 

                    Pas de consensus sur le prix idéal : Il n'y a pas de consensus sur le "prix idéal" du carbone, et il est possible qu'un tel prix n'existe pas. Cela dépend en grande partie des valeurs et des priorités de chaque économiste ou décideur politique. 
                    
                    Écart entre théorie et pratique : Malgré ces propositions, le prix réel du carbone reste nettement en deçà des prix théoriques suggérés, indiquant une divergence entre les politiques économiques et environnementales théoriques et pratiques. 
                    
                    La taxe carbone n'est pas une solution unique : La lutte contre le changement climatique nécessite une approche globale, qui comprend non seulement la tarification du carbone, mais aussi des politiques visant à favoriser les énergies renouvelables, à améliorer l'efficacité énergétique, à réduire les déchets et à protéger les écosystèmes. 
                    
                    Mise en œuvre progressive : Toute augmentation de la taxe carbone devrait être mise en œuvre de manière progressive, afin de minimiser l'impact sur les ménages à faible revenu et d'éviter les réactions défavorables. 
                    
                    Mesures compensatoires : Les hausses de la taxe carbone doivent être accompagnées de mesures compensatoires pour protéger les groupes les plus vulnérables, tels que les ménages à faible revenu, qui pourraient être disproportionnellement touchés par une augmentation des coûts de l'énergie</p>
                </div>
            </div>
           
            <div class="flex items-center">
                <img src="autrestarifs.png" alt="Image 1" class="w-16 h-16 mr-4">
                <div>
                  <h2 id="autres formes de tarification" class="text-xl font-bold mb-2">Ouverture sur d’autres formes de tarification  </h2>
                  <p class="text-gray-700 mb-4">Système d'échange de quotas d'émissions (SEQE) : Ce système, qui existe depuis environ une décennie, attribue des quotas d'émissions de gaz à effet de serre aux entreprises, qu'elles peuvent ensuite échanger. Les critiques soulignent que trop de quotas sont attribués, ce qui nécessite une régulation plus stricte. 

                    Normes de performance énergétique : Ces normes fixent des limites aux émissions de gaz à effet de serre pour les véhicules, les bâtiments et l'équipement, incitant les acteurs à opter pour les options les moins polluantes. Ces normes peuvent être basées sur la technologie actuellement disponible ou sur les meilleures pratiques du secteur. 
                    
                    Mécanisme d'ajustement carbone aux frontières : Ce mécanisme, engagé par l'Union européenne en 2022, vise à taxer les importations en provenance de pays où la taxe carbone est plus basse. Il vise à éviter le "dumping environnemental" et à promouvoir l'équité dans le commerce international. 
                    
                    Limites du mécanisme d'ajustement carbone : Le mécanisme d'ajustement carbone est toutefois limité, car il ne peut être appliqué à toutes les industries sans faire exploser les coûts pour les consommateurs. De plus, il est difficile de l'appliquer correctement en raison de l'opacité des procédés dans certains pays. 
                    
                    Adaptabilité des outils : L'application et l'efficacité de ces outils peuvent varier en fonction des spécificités de chaque pays et secteur. Par conséquent, il est nécessaire d'adapter les outils de tarification du carbone aux contextes locaux et sectoriels. 
                    
                    Complémentarité des outils : Au lieu de compter sur un seul outil, une combinaison de différents outils de tarification du carbone - tels que la taxe carbone, le SEQE et les normes de performance énergétique - peut fournir une approche plus complète et flexible pour réduire les émissions de gaz à effet de serre.  </p>
                </div>
            </div>
            <div class="flex items-center">
                <img src="methane.png" alt="Image 1" class="w-16 h-16 mr-4">
                <div>
                  <h2 id="méthane et kérozène" class="text-xl font-bold mb-2">Aller plus loin: taxer le méthane dans l’agriculture et le kérosène dans l'aviation  </h2>
                  <p class="text-gray-700 mb-4">Équilibrer la taxe carbone par secteur : Il est recommandé de fixer un seuil minimal croissant de taxe carbone pour les secteurs qui bénéficient actuellement de taux réduits ou d'exonérations, comme le transport routier, les services de taxi, l'agriculture et la navigation aérienne et maritime. 

                    Taxation de l'agriculture : L'agriculture est responsable d'une part importante des émissions de gaz à effet de serre. Taxer ces émissions pourrait inciter les agriculteurs à adopter des pratiques plus respectueuses de l'environnement. 
                    
                    Encourager des pratiques agricoles plus durables : La taxe carbone pourrait encourager la réduction des cheptels, la gestion plus efficace des déjections animales et l'utilisation de méthodes de production agricole plus durables. 
                    
                    Financement de la transition vers une agriculture durable : Le revenu généré par la taxe carbone pourrait être utilisé pour financer la transition vers une agriculture plus durable. 
                    
                    Mesures d'accompagnement : L'impact économique et social d'une telle taxe sur les agriculteurs et les communautés rurales doit être pris en compte. Des mesures d'accompagnement devraient être prévues pour aider les agriculteurs à s'adapter. 
                    
                    Équité fiscale : Les efforts de tarification du carbone doivent être équilibrés par des mesures pour atténuer les effets sur les ménages à faible revenu et les communautés vulnérables, afin de garantir une transition équitable vers une économie à faible émission de carbone. </p>
                </div>
            </div>
            {/if}
            {#if activeSection === 2}

            <div class="flex justify-center mt-10">
                <div class="w-1/3 px-4">
                  <a href="#seloncabinetdeconseil" class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mb-4">
                    ...selon les cabinets de conseil
                  </a>
                </div>
                <div class="w-1/3 px-4">
                  <a href="#selonONG" class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded mb-4">
                    ...selon les ONG
                  </a>
                </div>
                
            </div>

            <div class="flex items-center">
              <img src="conseil.png" alt="Image 2" class="w-16 h-16 mr-4">
              <div>
                <h2 id="seloncabinetdeconseil" class="text-xl font-bold mb-2">Selon les cabinets de conseil</h2>
                <p class="text-gray-700 mb-4">Proactivité des entreprises : Pour anticiper les nouvelles tarifications et réglementations, les entreprises doivent prendre une posture proactive, comprendre leur fonctionnement et agir en conséquence le plus tôt possible. 

                    Compréhension du système de taxation carbone : Les entreprises doivent s'efforcer de comprendre les subventions et les incitations fiscales offertes par les gouvernements liées à la taxe carbone. Cette compréhension pourrait aider à réduire les coûts à court terme et à orienter les opérations de l'entreprise vers des actions plus respectueuses de l'environnement à long terme. 
                    
                    Évaluation de l’impact de la taxe carbone et mise en place d’une stratégie de décarbonation : Les entreprises doivent évaluer l'impact de l'exposition à la taxation carbone sur leurs opérations à l'échelle nationale et internationale. Par la suite, elles doivent examiner comment réduire leur empreinte carbone tout au long de la chaîne de valeur, ce qui peut conduire à une réduction des coûts associés à la taxe carbone. 
                    
                    Communication et Responsabilité Sociale des Entreprises (RSE) : Il est important pour les entreprises de communiquer clairement sur leurs efforts de décarbonation et de les partager avec leurs parties prenantes, notamment les consommateurs et les actionnaires. 
                    
                    Prise en compte de l’impact financier de la taxe carbone : Les entreprises doivent évaluer l'impact financier de la taxe carbone sur leurs activités et cartographier ce risque de la manière la plus exhaustive possible. 
                    
                    Finance & Investissement : Le soutien aux investissements décarbonés est recommandé, en particulier pour les entreprises de secteurs à forte émission de carbone, pour réduire leur impact environnemental et ainsi atténuer leur exposition à la taxe carbone. </p>
              </div>
            </div>
            <div class="flex items-center">
                <img src="fondaquarelle.jpg" alt="Image 2" class="w-16 h-16 mr-4">
                <div>
                  <h2 id="selonONG" class="text-xl font-bold mb-2">Selon les ONG</h2>
                  <p class="text-gray-700 mb-4">Application du principe de "pollueur-payeur" : Il faut mettre fin à l'iniquité de la taxe carbone qui favorise actuellement les grandes entreprises polluantes. Un prix plancher du carbone doit être instauré pour que ces entreprises contribuent de manière équitable à la lutte contre le changement climatique. 

                    Instauration d'un revenu-climat : Le financement de ce revenu pourrait être assuré par les recettes générées par la taxe carbone, assurant ainsi une redistribution plus juste des coûts associés à la lutte contre le changement climatique. 
                    
                    Financement des grands projets de transition écologique : L'utilisation des recettes de la "contribution climat énergie solidarité" et de l'application du principe pollueur-payeur pourrait générer des fonds considérables pour financer la transition écologique. 
                    
                    Respect du principe "zéro chômeur dans la transition écologique" : Il est crucial de garantir que la transition vers une économie plus durable n'entraîne pas de pertes d'emplois. Des mesures de formation, de reconversion et de soutien à l'emploi doivent être mises en place pour les travailleurs et les secteurs touchés. 
                    
                    Augmentation du prix des quotas de CO2 : Le prix moyen d'un quota sur le marché du carbone a augmenté, générant ainsi plus de revenus pouvant être investis dans la transition écologique. 
                    
                    Envoi d'un signal prix fort aux pollueurs : L'application du principe pollueur-payeur augmenterait le coût des énergies fossiles, encourageant une transition écologique tout en respectant la justice sociale.  </p>
                </div>
              </div>
            {/if}
            {#if activeSection === 3}
           
            {/if}
          </div>
        </div>
      </div>
      
      
      {/if}
    </div>
  </main>
  
  <style>
    button {
      @apply bg-blue-600;
    }
    
    p {
      white-space: pre-line;
    }
    </style>