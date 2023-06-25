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
      let image = document.getElementById("imageToFade");
    if (image) {
      image.remove();
    }
    }
  </script>
  
  <main class="w-full h-full mt-28  bg-gradient-to-r from-green-200 py-10">
    <div class="relative top-64 px-10 mx-auto text-center  z-50">
      <div class="fixed w-full h-auto top-40 bg-gradient-to-r from-green-200 ">
        <div class="text-center">
          <h1 class="text-4xl font-bold mb-4 mt-10">Inspirez vous...</h1>
        </div>
      
        <div class=" flex justify-around mt-10">
          <div class="px-4">
            <button class="bg-green-500 hover:bg-green-600 transform hover:scale-105 transition-transform duration-200 text-white font-bold py-2 px-4 rounded mb-4" on:click={() => toggleSection(1)}>
            ...des économistes environnementaux
            </button>
          </div>
          <div class="px-4">
            <button class="bg-green-500 hover:bg-green-600 transform hover:scale-105 transition-transform duration-200 text-white font-bold py-2 px-4 rounded mb-4" on:click={() => toggleSection(2)}>
              ...des économistes écologiques
            </button>
          </div>
          <div class="px-4">
            <button class="bg-green-500 hover:bg-green-600 transform hover:scale-105 transition-transform duration-200 text-white font-bold py-2 px-4 rounded mb-4" on:click={() => toggleSection(3)}>
              ...du monde de l’entreprise
            </button>
          </div>
          <div class="px-4">
            <button class="bg-green-500 hover:bg-green-600 transform hover:scale-105 transition-transform duration-200 text-white font-bold py-2 px-4 rounded mb-4" on:click={() => toggleSection(4)}>
                ...de la sphère politique
            </button>
          </div>
          <div class="px-4">
            <button class="bg-green-500 hover:bg-green-600 transform hover:scale-105 transition-transform duration-200 text-white font-bold py-2 px-4 rounded mb-4" on:click={() => toggleSection(5)}>
                ... des ONG
            </button>
          </div>
        </div>
        <div class="flex justify-center  h-screen">
        <div class="blur-sm">
            <img id="imageToFade" src="Partagearbre.png" alt="Image 1" class="w-full object-cover  mr-4">
        </div>
      </div>
    </div>
      



      {#if activeSection !== null}
      <div class="flex justify-center mt-4">
        <div class="sticky top-80">
          <div class=" rounded-lg shadow-md">
            {#if activeSection === 1}

            <div class="fixed top-80 mt-7 flex justify-around w-full px-4">
              <div class="mb-10">
                <a href="#Jean-Charles Hourcade" class="pulse bg-green-500 hover:bg-green-600 text-white font-bold py-2 px-4 rounded mb-4">
                  Jean-Charles Hourcade
                </a>
              </div>
              <div class=" mb-10">
                <a href="#Jean Tirole" class="pulse bg-green-500 hover:bg-green-600 text-white font-bold py-2 px-4 rounded mb-4">
                  Jean Tirole
                </a>
              </div>
              <div class="mb-10">
                <a href="#Picketty" class="pulse bg-green-500 hover:bg-green-600 text-white font-bold py-2 px-4 rounded mb-4">
                  Picketty
                </a>
              </div>
              <div class="mb-10">
                <a href="#Pindick" class="pulse bg-green-500 hover:bg-green-600 text-white font-bold py-2 px-4 rounded mb-4">
                  Pindyck
                </a>
              </div>
            </div>

            <div class="">
              <div class="sticky top-96 flex items-center  bg-gradient-to-b from-green-200 via-white to-orange-200 z=20">
                <img src="hourcade.png" alt="Image 1" class="w-1/4 mr-4">
                <div>
                  <h2 id="Jean-Charles Hourcade" class="text-xl font-bold mb-2">Jean-Charles Hourcade</h2>
                  <p class="text-gray-700 mb-4 justify-text px-20">Jean-Charles Hourcade, économiste et spécialiste du changement climatique, dénonce le brouillage autour de la taxe carbone, souvent présentée comme punitivement antinomique avec l'économie et la justice sociale. 

                    Il réfute l'idée que la taxe carbone est punitive et culpabilisatrice, arguant qu'elle stimule l'innovation, modifie les comportements non durables et corrige les marchés défaillants. 
                    
                    Hourcade reconnaît que l'énergie est coûteuse, mais il attribue cette perception à l'inertie de la société qui s'est habituée à des coûts énergétiques faibles, entrainant une surconsommation. 
                    
                    Si la taxe carbone peut sembler impuissante à changer les comportements à court terme, une taxe progressive étalée dans le temps et étendue à plusieurs secteurs pourrait modifier profondément la consommation. 
                    
                    L'implémentation réussie de la taxe carbone nécessite une gouvernance efficace et une action collective, avec un prix unique à l'échelle européenne. 
                    
                    L'un des points clés pour allier questions sociales et fiscalité carbone en France serait l'utilisation des recettes de cette taxe à des fins sociales - par exemple, en réduisant les charges pour les foyers les plus affectés et à faibles revenus, pour favoriser l'emploi tout en luttant contre le changement climatique. </p>
                </div>
              </div>
            <div class="sticky top-96 flex items-center  bg-gradient-to-b from-green-200 via-white to-orange-200  z=30">
                
                <div>
                  <h2 id="Jean Tirole" class=" text-xl font-bold mb-2">Jean Tirole</h2>
                  <p class="text-gray-700 mb-4 justify-text px-20">Jean Tirole, économiste renommé, insiste sur l'importance de l'action collective européenne en matière de taxe carbone pour éviter les "fuites carbones", où les entreprises se délocalisent vers des régions moins taxées. 

                    Il propose la création d'une "Banque du Carbone", agissant de manière indépendante pour gérer et augmenter progressivement le tarif du carbone, analogique à une banque centrale. 
                    
                    Pour faire face aux inégalités, Tirole suggère de redistribuer les revenus en modifiant les taux d'imposition pour soutenir les ménages modestes tout en maintenant le prix du carbone, ou par la mise en place d'un revenu universel de base. 
                    
                    Il défend l'idée d'éviter une différenciation des prix du carbone entre les pays développés et en développement, optant plutôt pour des transferts financiers des pays riches vers les pays pauvres. 
                    
                    Tirole insiste sur le rôle des institutions internationales comme l'OMC ou le FMI pour sanctionner les pays qui ne respectent pas les règles du jeu. Cette démarche doit être progressivement mise en place, en commençant par l'Europe. 
                    
                    Il met également en lumière le rôle crucial des consommateurs en démocratie : le changement doit être soutenu par une prise de conscience collective, car les entreprises et les politiques s'alignent sur les demandes de leurs consommateurs et électeurs respectifs. </p>
                </div>
                <img src="tirole.png" alt="Image 1" class="w-1/4">
              </div>
            <div class="sticky top-96 flex items-center  bg-gradient-to-b from-green-200 via-white to-orange-200  z=40">
                <img src="picketty.png" alt="Image 1" class="w-1/4">
                <div>
                  <h2 id="Picketty" class="text-xl font-bold mb-2">Picketty</h2>
                  <p class="text-gray-700 mb-4 justify-text px-20">
                    
                    Thomas Piketty, expert reconnu des inégalités économiques, remet en question l'impact équitable de la taxe carbone, en soulignant les inégalités qu'elle peut causer, en particulier pour les ménages les plus modestes. 
                    
                    Il propose une taxe carbone progressive, indexée sur le niveau de revenu, pour atténuer ces inégalités. Selon lui, cette taxe doit différencier ceux qui émettent peu de CO2 de ceux qui en émettent beaucoup. 
                    
                    Piketty défend l'idée que cette taxe devrait être mise en place à une échelle mondiale, commençant d'abord au niveau européen, pour une efficacité maximale. 
                    
                    Il soutient l'idée d'un ajustement du barème de l'impôt sur le revenu pour neutraliser l'effet de la taxe carbone sur les ménages les plus modestes, réduisant ainsi son impact inégalitaire. 
                    
                    Il propose une taxe progressive sur les émissions, sans taxe sur les premières tonnes émises, puis avec une augmentation progressive jusqu'à des niveaux d'émissions maximum, après lesquels une amende remplacerait la taxe. 
                    
                    L'approche de Piketty se concentre sur les inégalités entre les individus plutôt qu'entre les pays, un changement de perspective qui reconnaît les disparités de revenus et de consommation d'énergie à l'échelle mondiale. </p>
                </div>
            </div>
            <div class="sticky top-96 flex items-center  bg-gradient-to-b from-green-200 via-white to-orange-200 z=50">
                
                <div>
                  <h2 id="Pindick" class="text-xl font-bold mb-2 ">Pindyck</h2>
                  <p class="text-gray-700 mb-4 justify-text px-20">Robert S. Pindyck critique les modèles d'évaluation intégrée (IAMs) pour estimer le coût social du carbone (CSC), soulignant leur manque de fiabilité à cause des hypothèses arbitraires qu'ils requièrent. 

                    Les IAMs sont composés de plusieurs éléments, notamment des projections d'émissions futures de CO2 et de leurs impacts économiques. Cependant, les modèles peuvent varier considérablement en fonction des hypothèses faites, en particulier en ce qui concerne la fonction de bien-être social et son taux de préférence temporelle. 
                    
                    Pindyck souligne les différences significatives dans les estimations du CSC entre différents économistes, en particulier entre Nordhaus et Stern, qui se sont basés sur des hypothèses différentes concernant le taux de préférence temporelle. 
                    
                    Malgré l'accord sur ces hypothèses, Pindyck soutient que les IAMs ne peuvent pas produire une bonne estimation du CSC, principalement en raison de la difficulté de mesurer la sensibilité du climat et l'ignorance des IAMs des résultats climatiques catastrophiques. 
                    
                    Pour surmonter ces limites, Pindyck recommande d'envisager une gamme plausible de résultats catastrophiques et leur probabilité associée, puis de calculer la valeur actuelle des avantages découlant de l'évitement de ces résultats ou de la réduction de leur probabilité d'occurrence. 
                    
                    En dépit de l'incertitude entourant l'estimation du CSC, Pindyck suggère de commencer par une petite taxe sur le carbone pour reconnaître le coût social du carbone, puis d'ajuster cette taxe à mesure que nous en apprenons davantage sur le véritable coût du carbone. </p>
                </div>
                <img src="pindick.png" alt="Image 1" class="w-1/4">
            </div>
            </div>
            {/if}
            {#if activeSection === 2}

            <div class="fixed top-80 mt-7 flex justify-around w-full px-4">
              <div class="mb-10">
                <a href="#Jean-Charles Hourcade" class="pulse bg-green-500 hover:bg-green-600 text-white font-bold py-2 px-4 rounded mb-4">
                  Porcher
                </a>
              </div>
              <div class=" mb-10">
                <a href="#Jean Tirole" class="pulse bg-green-500 hover:bg-green-600 text-white font-bold py-2 px-4 rounded mb-4">
                  Parrique
                </a>
              </div>
  
          </div>

          <div class="">
          <div class="sticky top-96 flex items-center  bg-gradient-to-b from-green-200 via-white to-orange-200 z=20">
            <img src="porcher.png" alt="Image 1" class="w-1/4 mr-4">
            <div>
              <h2 id="Jean-Charles Hourcade" class="text-xl font-bold mb-2">Porcher</h2>
              <p class="text-gray-700 mb-4 justify-text px-20">Thomas Porcher, économiste français engagé, estime que la taxe carbone actuelle est inéquitable car elle ne prend pas en compte la "situation économique et géographique" des individus. 

                Selon lui, la taxe carbone affecte davantage les foyers modestes que les foyers aisés, ce qui va à l'encontre du principe du "pollueur-payeur". 
                
                Porcher souligne que la capacité d'adaptation des consommateurs est faible à court terme, et qu'une hausse de la taxe carbone entraînerait une forte opposition de la population, comme l'a démontré le mouvement des Gilets Jaunes. 
                
                Pour rendre la taxe carbone plus équitable, Porcher suggère d'augmenter la taxation pour ceux qui ont accès à des modes de transport alternatifs mais qui choisissent malgré tout des "véhicules à forte cylindrée". 
                
                Cette approche permettrait d'inciter les individus à modifier leur comportement, et serait plus conforme au principe du "pollueur-payeur". 
                
                En conclusion, Porcher préconise une taxe carbone flexible qui tiendrait compte de la situation des individus, bien que cette proposition puisse être difficile à mettre en œuvre en pratique.</p>
            </div>
          </div>
          <div class="sticky top-96 flex items-center  bg-gradient-to-b from-green-200 via-white to-orange-200  z=30">
              
              <div>
                <h2 id="Jean Tirole" class=" text-xl font-bold mb-2">Parrique</h2>
                <p class="text-gray-700 mb-4 justify-text px-20">Timothée Parrique, chercheur et activiste français, critique l'idée qu'une économie puisse continuer à croître tout en réduisant son empreinte écologique, un concept connu sous le nom de "découplage". 

                  Il soutient que la taxe carbone, bien que souvent considérée comme un outil pour encourager la réduction de l'empreinte écologique, n'est qu'un instrument parmi d'autres, et pas nécessairement le meilleur. Il mentionne l'exemple de la Suède où une taxe carbone n'a pas réussi à décarboner l'économie. 
                  
                  Pour Parrique, un système de quotas carbone sous forme de permis, appliqué à l'ensemble de l'économie, serait une solution plus appropriée pour aborder le problème du changement climatique. 
                  
                  Il préconise également des mesures d'interdiction, comme l'interdiction des véhicules thermiques et de la publicité associée, ainsi que des politiques ciblées, comme une stratégie de décroissance du secteur de l'aviation commerciale. 
                  
                  Selon Parrique, se concentrer uniquement sur la taxe carbone et la croissance verte serait insuffisant face à la gravité du défi climatique. 
                  
                  En conclusion, il semble que Parrique plaide pour une approche intégrée et radicale pour allier questions sociales et fiscalité carbone, incluant des quotas carbone, des interdictions spécifiques et une réorientation des secteurs les plus polluants. </p>
              </div>
              <img src="parrique.png" alt="Image 1" class="w-1/4">
            </div>
          
          </div>

            {/if}


            
            {#if activeSection === 3}

            <div class="fixed top-80 mt-7 flex justify-around w-full px-4">
              <div class="mb-10">
                <a href="#Cabinets de conseil" class="pulse bg-green-500 hover:bg-green-600 text-white font-bold py-2 px-4 rounded mb-4">
                  Cabinets de conseil
                </a>
              </div>
              <div class=" mb-10">
                <a href="#parrique" class="pulse bg-green-500 hover:bg-green-600 text-white font-bold py-2 px-4 rounded mb-4">
                  Chambre de commerce et d’industrie
                </a>
              </div>
  
          </div>

          <div class="">
          <div class="sticky top-96 flex items-center  bg-gradient-to-b from-green-200 via-white to-orange-200 z=20">
            <img src="conseil.png" alt="Image 1" class="w-1/4 mr-4">
            <div>
              <h2 id="Cabinets de conseil" class="text-xl font-bold mb-2">Cabinets de conseil</h2>
              <p class="text-gray-700 mb-4 justify-text px-20">Prix du Carbone : Les cabinets de conseil KPMG et EY soulignent l'importance d'un prix stable pour le carbone comme incitatif pour changer les comportements des entreprises, malgré le risque d'impact disproportionné sur les petites entreprises et le risque de fuites de carbone en cas de hausse de prix dans un seul pays. 

                Implications Financières : Les entreprises devront intégrer ce nouveau coût, le prix du carbone, dans leur modèle économique. Cela nécessitera une étroite collaboration entre les équipes fiscales et les dirigeants pour comprendre comment cette taxe affectera les prix finaux pour les consommateurs. 
                
                Impact sur le Chiffre d'Affaires : Une étude d'ECOACT révèle que le coût du carbone pourrait atteindre plus de 10% du chiffre d'affaires des secteurs les plus dépendants des énergies fossiles d'ici 2030, avec des implications majeures pour la cimenterie, la métallurgie, les services publics, le transport et la production d'énergie. 
                
                Coûts de Production : EY a montré qu'une taxe carbone de 25 dollars/tCO2eq aux Etats-Unis pourrait entraîner une augmentation moyenne de 0,7% des coûts de production dans 8 industries majeures et leurs sous-industries. Cet effet pourrait probablement se retrouver en France. 
                
                Impact sur la Chaîne de Valeur : Les études soulignent que l'impact de la taxe carbone ne se limite pas aux entreprises directement soumises à un prix réglementaire du carbone. Les secteurs moins carbonés peuvent également être touchés en raison de la répercussion du coût du carbone au sein des chaînes de valeur (scope 3). 
                
                Questions Sociales et Fiscalité Carbone : Pour allier les questions sociales et la fiscalité carbone en France, il faut tenir compte de la capacité des entreprises à répercuter le coût de la taxe sur leurs clients, de l'impact potentiel sur le pouvoir d'achat des consommateurs, et de l'importance d'appliquer des stratégies d'atténuation pour les secteurs et les entreprises les plus touchés.</p>
            </div>
          </div>
          <div class="sticky top-96 flex items-center  bg-gradient-to-b from-green-200 via-white to-orange-200  z=30">
              
              <div>
                <h2 id="Chambre de commerce et d’industrie" class=" text-xl font-bold mb-2">Chambre de commerce et d’industrie</h2>
                <p class="text-gray-700 mb-4 justify-text px-20">Transition équitable : La Chambre de Commerce et d'Industrie (CCI) soutient la transition écologique mais insiste sur une mise en œuvre équitable pour les entreprises de toutes tailles. 

                  Accompagnement des PME : La CCI prône une mise en place progressive de la taxe carbone, avec des mesures d'accompagnement spécifiques pour les petites et moyennes entreprises, potentiellement les plus affectées par l'augmentation des coûts énergétiques. 
                  
                  Financement de la transition : Les recettes de la taxe carbone, selon la CCI, devraient servir à financer des politiques de transition écologique et des mesures d'accompagnement pour les entreprises. 
                  
                  Harmonisation européenne : Pour éviter les distorsions de concurrence, la CCI recommande une harmonisation de la taxe carbone au niveau européen. 
                  
                  Responsabilité des entreprises : La CCI encourage les entreprises à prendre en compte leur responsabilité sociale et environnementale en adoptant des pratiques plus durables. 
                  
                  Préparation au changement climatique : Adopter des pratiques plus durables permettra aux entreprises de mieux se préparer aux défis du changement climatique tout en améliorant leur image auprès des clients et des parties prenantes. </p>
              </div>
              <img src="chambredecommerce.png" alt="Image 1" class="w-1/4">
            </div>
          
          </div>


            {/if}
            {#if activeSection === 4}
            
            <div class="fixed top-80 mt-7 flex justify-around w-full px-4">
              <div class="mb-10">
                <a href="#MEDEF" class="pulse bg-green-500 hover:bg-green-600 text-white font-bold py-2 px-4 rounded mb-4">
                  MEDEF
                </a>
              </div>
              <div class=" mb-10">
                <a href="#Syndicats des travailleurs" class="pulse bg-green-500 hover:bg-green-600 text-white font-bold py-2 px-4 rounded mb-4">
                  Syndicats des travailleurs
                </a>
              </div>
              <div class="mb-10">
                <a href="#Candidats à la présidentielle" class="pulse bg-green-500 hover:bg-green-600 text-white font-bold py-2 px-4 rounded mb-4">
                  Candidats à la présidentielle
                </a>
              </div>
              
          </div> 

          <div class="">
          <div class="sticky top-96 flex items-center  bg-gradient-to-b from-green-200 via-white to-orange-200 z=20">
            <img src="medef.png" alt="Image 1" class="w-1/4 mr-4">
            <div>
              <h2 id="MEDEF" class="text-xl font-bold mb-2">MEDEF</h2>
              <p class="text-gray-700 mb-4 justify-text px-20">Instabilité Fiscale: L'instabilité due à la crise des gilets jaunes et l'augmentation de la taxe carbone sont vues comme des défis par les entrepreneurs français. 

                Maintien de la Fiscalité: Les entrepreneurs français souhaitent maintenir la stabilité fiscale et juridique pour planifier l'avenir et éviter une augmentation de leur niveau d'imposition. 
                
                Acceptation de la Taxe Carbone: Le MEDEF n'est pas opposé à la taxe carbone, reconnaissant l'importance de préparer la transition énergétique avec une fiscalité dédiée. 
                
                Croissance et Décarbonation: Pour le MEDEF, il ne peut y avoir de décarbonation sans croissance économique. 
                
                Redistribuer les Taxes: Le MEDEF propose qu'un euro de taxe carbone devrait correspondre à un euro de taxe en moins ailleurs. 
                
                Planification de la Transition: Le MEDEF souligne l'importance d'avoir des calendriers pour la progression de la taxe carbone, afin que les entreprises puissent anticiper leurs actions, ces calendriers devant être compatibles avec l'état de la technologie. </p>
            </div>
          </div>
          <div class="sticky top-96 flex items-center  bg-gradient-to-b from-green-200 via-white to-orange-200  z=30">
              
              <div>
                <h2 id="Syndicats des travailleurs" class=" text-xl font-bold mb-2">Syndicats des travailleurs</h2>
                <p class="text-gray-700 mb-4 justify-text px-20">Soutien de la CFDT: Le syndicat, dirigé par Laurent Berger, soutient une taxe carbone, la jugeant nécessaire pour financer la transition écologique. 

                  Compensation pour les Ménages Modestes: La CFDT estime qu'il est crucial de mettre en place un mécanisme de compensation pour les ménages les plus modestes afin de contrebalancer les coûts de la taxe carbone. 
                  
                  Opposition de la CGT: La CGT est contre la composante carbone telle qu'elle est actuellement conçue, appelant à une réforme plus globale de la fiscalité. 
                  
                  Taxation du Capital: La CGT propose de taxer davantage ceux qui ont le plus de moyens, suggérant une taxation accrue du capital plutôt que du travail. 
                  
                  Allégement des Taxes Indirectes: La CGT propose un allégement des taxes indirectes, qui pèsent plus lourdement sur les ménages modestes. 
                  
                  Taxation des Entreprises et Transactions Financières: La CGT suggère une responsabilisation accrue des entreprises et une taxation des transactions financières pour financer la transition écologique.</p>
              </div>
              <img src="cgtcfdt.png" alt="Image 1" class="w-1/4">
            </div>
          <div class="sticky top-96 flex items-center  bg-gradient-to-b from-green-200 via-white to-orange-200  z=40">
              <img src="presidentielles2022.png" alt="Image 1" class="w-1/4">
              <div>
                <h2 id="Candidats à la présidentielle" class="text-xl font-bold mb-2">Candidats à la présidentielle</h2>
                <p class="text-gray-700 mb-4 justify-text px-20">
                  
                  Marine Le Pen (Rassemblement National): 

                        Préconise une réduction de la taxe TICPE sur les carburants pour préserver le pouvoir d'achat. 
                        
                        Cherche à atténuer l'impact de la hausse des prix du carburant sur les ménages français. 
                        
                         
                        
                        Anne Hidalgo (Parti Socialiste): 
                        
                        Soutient une transition écologique "sociale" qui protège les populations les plus fragiles. 
                        
                        Propose un ISF climatique "fléché vers les projets environnementaux, mais dans l'accompagnement social". 
                        
                         
                        
                        Yannick Jadot (Verts): 
                        
                        Prône un mécanisme d'ajustement carbone aux frontières de l'Europe, s'appliquant à tous les secteurs et incluant les émissions indirectes. 
                        
                        S'engage à instaurer un ISF climatique dès le début de son mandat, incluant une prise en compte de l'empreinte carbone. 
                        
                         
                        
                        Eric Zemmour (Reconquête): 
                        
                        Défend une taxe carbone aux frontières de l'Europe. 
                        
                        Vise à protéger les industries françaises contre la concurrence déloyale internationale. 
                        
                         
                        
                        Valérie Pécresse (Républicains): 
                        
                        Favorable à une taxe carbone aux frontières de l'Europe pour préserver la souveraineté économique française. 
                        
                        Voit cette taxe comme une "barrière écologique" contre la concurrence déloyale des pays non respectueux de l'environnement. 
                        
                         
                        
                        Jean-Luc Mélenchon (La France Insoumise): 
                        
                        Propose une "taxe kilométrique" aux frontières de la France, plutôt qu'aux frontières de l'UE. 
                        
                        Envisage le rétablissement et le renforcement de l'ISF, avec un "volet climatique" pour taxer les gros pollueurs.</p>
              </div>
          </div>
        </div>
        
            {/if}

            {#if activeSection === 5}
            
            <div class="fixed top-80 flex justify-around w-full px-4 mt-10">
                <div class="px-4 mb-10">
                  <a href="#Réseau climat France" class="pulse bg-green-500 hover:bg-green-600 text-white font-bold py-2 px-4 rounded mb-4">
                    Réseau climat France
                  </a>
                </div>
                <div class="px-4 mb-10">
                  <a href="#OXFAM" class="pulse bg-green-500 hover:bg-green-600 text-white font-bold py-2 px-4 rounded mb-4">
                    OXFAM
                  </a>
                </div>
                <div class="px-4 mb-10">
                  <a href="#ATTAC" class="pulse bg-green-500 hover:bg-green-600 text-white font-bold py-2 px-4 rounded mb-4">
                    ATTAC
                  </a>
                </div>
                <div class="px-4 mb-10">
                  <a href="#Greenpeace" class="pulse bg-green-500 hover:bg-green-600 text-white font-bold py-2 px-4 rounded mb-4">
                    Greenpeace
                  </a>
                </div>
                <div class="px-4 mb-10">
                    <a href="#Fondation Nicolas Hulot" class="pulse bg-green-500 hover:bg-green-600 text-white font-bold py-2 px-4 rounded mb-4">
                        Fondation Nicolas Hulot
                    </a>
                  </div>
                  <div class="px-4 mb-10">
                    <a href="#WWF" class="pulse bg-green-500 hover:bg-green-600 text-white font-bold py-2 px-4 rounded mb-4">
                        WWF
                    </a>
                  </div>
            </div>

            
        
            <div class="flex items-center">
                <img src="reseauclimat.png" alt="Image 3" class="w-1/3 h-1/3 mr-4 border-solid border-2 ">
                <div class=" bg-gradient-to-b from-green-200 via-white to-orange-200 ">
                  <h2 id="Réseau climat France  " class="text-xl font-bold mx-4 text-center py-4 ">Réseau climat France</h2>
                  <p class="text-gray-700 mb-4 mx-4 text-justify">Prise de conscience : Le Réseau Action Climat France, collectif composé de 37 associations, est conscient des impacts négatifs du changement climatique et soutient des mesures pour l'environnement, l'emploi, la santé et la justice sociale. 

                    Transition juste : Le collectif promeut une transition équitable vers une société plus durable, bénéfique à toutes les parties prenantes. 
                    
                    Position sur la CCE : Le réseau est en faveur de la Contribution Climat Énergie (CCE) ou taxe carbone, car elle encourage les ménages et les entreprises à adopter des comportements plus durables. 
                    
                    Mise en œuvre équitable : Cependant, ils insistent sur la nécessité d'implémenter cette taxe de manière juste et équitable pour éviter de pénaliser les ménages les plus modestes. 
                    
                    Utilisation des revenus : Le réseau préconise que les revenus de la CCE soient utilisés pour financer des mesures sociales aidant les ménages précaires dans la transition écologique. 
                    
                    Revenu climatique : Ils proposent l'introduction d'un "revenu climatique", redistribuant une partie des revenus de la taxe carbone aux ménages les plus pauvres sous forme de crédits d'impôts. </p>
                </div>
              </div>
              <div class="flex items-center">
                
                <div class="bg-gradient-to-b from-orange-200 via-white to-rose-200">
                  <h2 id="OXFAM" class="text-xl font-bold mx-4 text-center py-4">OXFAM</h2>
                  <p class="text-gray-700 mb-4 mx-4 text-justify">ONG engagée : OXFAM, organisation non gouvernementale internationale, lutte contre la pauvreté et les injustices mondiales et soutient les efforts contre le changement climatique. 

                    Soutien à la CCE : Oxfam approuve la Contribution Climat Énergie (CCE) ou taxe carbone comme moyen efficace d'encourager les ménages et les entreprises à diminuer leur consommation de combustibles fossiles. 
                    
                    Sensibilité sociale : Cependant, Oxfam insiste sur l'évaluation des impacts de la taxe carbone pour éviter de pénaliser les ménages les plus vulnérables et les plus pauvres. 
                    
                    Redistribution des revenus : L'organisation préconise que les revenus de la taxe carbone soient utilisés pour combattre la pauvreté et les inégalités, et soutenir la transition vers une économie bas-carbone. 
                    
                    Protection des plus vulnérables : Selon Oxfam, la taxe carbone doit être mise en place de manière juste et équitable pour lutter efficacement contre le changement climatique tout en protégeant les populations les plus vulnérables. 
                    
                    Équité : En résumé, Oxfam plaide pour une taxe carbone équitable qui favorise à la fois l'environnement et la justice sociale. </p>
                </div>
                <img src="oxfam.png" alt="Image 3" class="w-1/3 h-1/3 mr-4">
              </div>
              <div class="flex items-center">
                <img src="attac.png" alt="Image 3" class="w-1/5 h-1/5 mr-4">
                <div class="bg-gradient-to-b from-rose-200 via-white to-violet-200">
                  <h2 id="ATTAC" class="text-xl font-bold mx-4 text-center py-4">ATTAC</h2>
                  <p class="text-gray-700 mb-4 mx-4 text-justify">Approche multidimensionnelle : ATTAC, ONG altermondialiste, souligne que la taxe carbone n'est qu'une partie de la solution au changement climatique. D'autres mesures, comme la réglementation des émissions de CO2 et la transition vers les énergies renouvelables, sont également nécessaires. 

                    Transition écologique socialement équitable : Selon ATTAC, la transition écologique doit se faire de manière socialement juste, avec une redistribution équitable des revenus générés par la taxe carbone. 
                    
                    Financement de la transition énergétique : Les revenus de la taxe carbone devraient servir à financer des programmes de transition énergétique, tels que la rénovation thermique des bâtiments et le développement des énergies renouvelables. 
                    
                    Prise en compte des populations vulnérables : Une politique de redistribution équitable est essentielle pour garantir une transition juste pour tous, en particulier pour les personnes économiquement et socialement vulnérables. 
                    
                    Équilibre entre efficacité environnementale et justice sociale : ATTAC souligne la nécessité de trouver un équilibre entre l'efficacité environnementale de la taxe carbone et la justice sociale. 
                    
                    Coopération internationale : ATTAC insiste également sur l'importance de prendre en compte les questions de coopération internationale afin que la transition écologique ne se fasse pas au détriment des pays en développement. </p>
                </div>
              </div>
              <div class="flex items-center">
                
                <div class="bg-gradient-to-b from-violet-200 via-white to-green-200">
                  <h2 id="Greenpeace" class="text-xl font-bold mx-4 text-center py-4">Greenpeace</h2>
                  <p class="text-gray-700 mb-4 mx-4 text-justify">Position initiale : Greenpeace a salué l'introduction de la taxe carbone en France en 2014 comme un pas vers la lutte contre le changement climatique et la promotion d'une économie verte, tout en mettant en évidence la nécessité de mesures d'accompagnement social. 

                    Critiques : L'organisation a critiqué la taxe carbone française pour son insuffisance à atteindre les objectifs climatiques, en soulignant également l'injustice des exemptions accordées aux grandes entreprises émettrices. 
                    
                    Redéploiement des recettes : Greenpeace propose d'utiliser les revenus de la taxe carbone pour financer la transition vers une économie verte, stimuler la production d'énergies renouvelables et soutenir les communautés affectées par ces changements. 
                    
                    Les milliardaires et le climat : Greenpeace souligne que les individus extrêmement riches ont une empreinte carbone disproportionnée et donc une responsabilité importante dans la lutte contre le changement climatique. 
                    
                    Rôle des plus riches : L'organisation fait valoir que cette élite économique possède les moyens financiers et l'influence nécessaires pour investir massivement dans des technologies et projets liés aux énergies renouvelables. 
                    
                    L'ISF Climatique : Greenpeace propose une redistribution plus équitable des richesses par le biais d'un "ISF Climatique", faisant partie d'un effort plus large pour lutter contre le changement climatique et investir dans une économie verte et équitable. </p>
                </div>
                <img src="greenpeace.png" alt="Image 3" class="w-1/3 h-1/3 mr-4">
              </div>
              <div class="flex items-center">
                <img src="FNH.png" alt="Image 3" class="w-1/3 h-1/3 mr-4">
                <div class="bg-gradient-to-b from-green-200 via-white to-orange-200">
                  <h2 id="Fondation Nicolas Hulot" class="text-xl font-bold mx-4 text-center py-4">Fondation Nicolas Hulot</h2>
                  <p class="text-gray-700 mb-4 mx-4 text-justify">Préambule : La Fondation pour la Nature et l'Homme (FNH), fondée par l'écologiste Nicolas Hulot, est dédiée à la protection de l'environnement et à la lutte contre le changement climatique, avec des initiatives allant de la protection de la biodiversité à la transition énergétique. 

                    La taxe carbone : La FNH voit la taxe carbone comme un outil important pour encourager la transition vers une économie décarbonée, mais souligne qu'elle doit être conçue de manière équitable. 
                    
                    Les ménages pauvres et vulnérables : Ces ménages sont souvent contraints d'utiliser des moyens de transport polluants et ne peuvent pas se permettre des alternatives plus propres. La FNH plaide pour des mesures compensatoires pour ces ménages face à la hausse des coûts induite par la taxe carbone. 
                    
                    Critique de l'injustice : La FNH soutient que la taxe carbone peut être discriminatoire en affectant de manière disproportionnée les ménages modestes, tandis que les grandes entreprises peuvent souvent échapper à cette taxe ou bénéficier de dérogations. 
                    
                    Utilisation des revenus de la taxe : La FNH estime que les revenus de la taxe carbone ne devraient pas être utilisés pour réduire le déficit budgétaire ou financer d'autres politiques gouvernementales, mais pour encourager les transitions vers des économies vertes et durables. 
                    
                    Propositions de réformes : Pour rendre la taxe carbone plus équitable, la FNH propose d'utiliser ses revenus pour financer des initiatives sociales et environnementales qui aident les ménages à faible revenu à effectuer cette transition, tout en mettant en garde contre les conséquences négatives de la taxe sur les populations vulnérables. </p>
                </div>
              </div>

              <div class="flex items-center">
                
                <div class="bg-gradient-to-b from-orange-200 via-white to-rose-200">
                  <h2 id="WWF" class="text-xl font-bold mx-4 text-center py-4">WWF</h2>
                  <p class="text-gray-700 mb-4 mx-4 text-justify">Introduction : Le World Wide Fund for Nature (WWF) est une ONG environnementale internationale dédiée à la conservation de la biodiversité et à l'utilisation durable des ressources naturelles. 

                    La taxe carbone : Le WWF soutient la taxe carbone en tant qu'outil efficace pour réduire les émissions de gaz à effet de serre et lutter contre le changement climatique, mais insiste sur sa mise en œuvre de manière socialement équitable. 
                    
                    Prise en compte des ménages vulnérables : Le WWF souligne que la taxe carbone ne doit pas peser indûment sur les ménages vulnérables et doit encourager les investissements dans les énergies renouvelables et les mesures d'efficacité énergétique. 
                    
                    Utilisation des revenus de la taxe : Les autorités devraient utiliser les revenus générés par la taxe carbone pour financer des projets de développement durable, notamment la production d'énergie renouvelable, l'amélioration de l'efficacité énergétique et des projets d'adaptation aux effets du changement climatique pour les communautés les plus sensibles. 
                    
                    Impact social de la taxe : Pierre Cannet, du WWF France, a souligné que, bien que la taxe carbone soit essentielle pour la transition vers une économie bas carbone, son impact social doit être pris en compte et compensé pour les ménages les plus modestes. 
                    
                    Appel à une réflexion plus large : Le WWF appelle à une réflexion plus large sur la fiscalité écologique, la combinant avec des mesures de redistribution pour réduire les inégalités sociales et économiques, tout en encourageant les politiques à s'engager dans une véritable transition énergétique.</p>
                </div>
                <img src="WWF.png" alt="Image 3" class="w-96  h-96 mr-4">
            </div>

            {/if}
          </div>
        </div>
      </div>
      {/if}
    </div>
  </main>
  
  <style>
   @keyframes pulse {
  0% { transform: scale(1); background-color: #48BB78;}
  50% { transform: scale(1.1); background-color: #000000; }
  100% { transform: scale(1); background-color: #ECC94B;}
}

.pulse {
  animation: pulse 1s infinite;
}

    p {
      white-space: pre-line;
    }

    .anchor {
        scroll-margin-top: b-8; 
    }

  
    </style>