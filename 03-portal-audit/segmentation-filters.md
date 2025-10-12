# Audience Segmentation Filters - Complete Tree

**Page**: Community (`/analytics`)
**Feature**: Audience Segmentation Dialog
**Access**: "All segments" button
**Date Documented**: 2025-10-10
**Screenshot**: `filter-location-section.png`

---

## Overview

O sistema de segmentação de audiência permite filtrar a comunidade por múltiplas dimensões usando operadores lógicos (AND/OR). A estrutura é hierárquica: **Section → Category → Options**.

**Total Structure**:
- **6 Sections** (top-level groupings)
- **10 Categories** (mid-level filters)
- **~263+ individual options** (specific filter values)

---

## Filter Operators

**Operator Selection**: AND / OR
- **AND (+)**: Todas as condições devem ser satisfeitas (intersecção)
- **OR (∪)**: Qualquer condição pode ser satisfeita (união)

---

## Complete Segmentation Tree

### 1. Demographics (4 categories, 21 options)

Filtros baseados em características demográficas da audiência.

#### 1.1 Gender (3 options)
- female
- male
- other

#### 1.2 Age Category (5 options)
- Adult
- Child
- Senior/Elderly
- Teenager/Adolescent
- Young Adult

#### 1.3 Ethnicity (8 options)
- African
- Asian
- Caucasian
- Indigenous
- Latino/Hispanic
- Middle Eastern
- Pacific Islander
- Southern Asian

#### 1.4 Social Status (5 options)
- Lower Class
- Lower-Middle Class
- Middle Class
- Upper Class
- Upper-Middle Class

**Total Demographics Options**: 21

---

### 2. Location (2 categories, 203 options)

Filtros baseados em localização geográfica dos utilizadores.

#### 2.1 Location (Country) (197 options)
- Afghanistan
- Albania
- Algeria
- Andorra
- Angola
- Antigua and Barbuda
- Argentina
- Armenia
- Australia
- Austria
- Azerbaijan
- Bahamas
- Bahrain
- Bangladesh
- Barbados
- Belarus
- Belgium
- Belize
- Benin
- Bhutan
- Bolivia
- Bosnia and Herzegovina
- Botswana
- Brazil
- Brunei
- Bulgaria
- Burkina Faso
- Burundi
- Cabo Verde
- Cambodia
- Cameroon
- Canada
- Central African Republic
- Chad
- Chile
- China
- Colombia
- Comoros
- Congo
- Costa Rica
- Croatia
- Cuba
- Cyprus
- Czechia
- Democratic Republic of the Congo
- Denmark
- Djibouti
- Dominica
- Dominican Republic
- East Timor
- Ecuador
- Egypt
- El Salvador
- Equatorial Guinea
- Eritrea
- Estonia
- Eswatini
- Ethiopia
- Fiji
- Finland
- France
- Gabon
- Gambia
- Georgia
- Germany
- Ghana
- Greece
- Grenada
- Guatemala
- Guinea
- Guinea-Bissau
- Guyana
- Haiti
- Honduras
- Hungary
- Iceland
- India
- Indonesia
- Iran
- Iraq
- Ireland
- Israel
- Italy
- Ivory Coast
- Jamaica
- Japan
- Jordan
- Kazakhstan
- Kenya
- Kiribati
- Kosovo
- Kuwait
- Kyrgyzstan
- Laos
- Latvia
- Lebanon
- Lesotho
- Liberia
- Libya
- Liechtenstein
- Lithuania
- Luxembourg
- Madagascar
- Malawi
- Malaysia
- Maldives
- Mali
- Malta
- Marshall Islands
- Mauritania
- Mauritius
- Mexico
- Micronesia
- Moldova
- Monaco
- Mongolia
- Montenegro
- Morocco
- Mozambique
- Myanmar
- Namibia
- Nauru
- Nepal
- Netherlands
- New Zealand
- Nicaragua
- Niger
- Nigeria
- North Korea
- North Macedonia
- Norway
- Oman
- Pakistan
- Palau
- Palestine
- Panama
- Papua New Guinea
- Paraguay
- Peru
- Philippines
- Poland
- Portugal
- Qatar
- Romania
- Russia
- Rwanda
- Saint Kitts and Nevis
- Saint Lucia
- Saint Vincent and the Grenadines
- Samoa
- San Marino
- Sao Tome and Principe
- Saudi Arabia
- Senegal
- Serbia
- Seychelles
- Sierra Leone
- Singapore
- Slovakia
- Slovenia
- Solomon Islands
- Somalia
- South Africa
- South Korea
- South Sudan
- Spain
- Sri Lanka
- Sudan
- Suriname
- Sweden
- Switzerland
- Syria
- Taiwan
- Tajikistan
- Tanzania
- Thailand
- Togo
- Tonga
- Trinidad and Tobago
- Tunisia
- Turkey
- Turkmenistan
- Tuvalu
- Uganda
- Ukraine
- United Arab Emirates
- United Kingdom
- United States
- Uruguay
- Uzbekistan
- Vanuatu
- Vatican City
- Venezuela
- Vietnam
- Yemen
- Zambia
- Zimbabwe

#### 2.2 Continent (6 options)
- Africa
- Asia
- Europe
- North America
- Oceania
- South America

**Total Location Options**: 203

---

### 3. Psychographics (2 categories, 30 options)

Filtros baseados em características psicológicas e de estilo de vida.

#### 3.1 Lifestyle (5 options)
- Active/Sporty
- Adventurous/Explorer
- Cultural/Creative
- Family-oriented
- Luxurious/High-end

#### 3.2 Industry (25 options)
- Administrative services
- Agriculture/fishing/forestry
- Architecture/engineering
- Arts/entertainment/sports/multimedia
- Business and finance
- Business decision makers
- Cleaning/maintenance services
- Community/social assistance
- Computing/mathematics
- Construction/extraction
- Education/libraries
- Food/restaurants
- Installation/repair services
- IT decision makers
- Legal services
- Life/physical/social sciences
- Management
- Manufacturing
- Medical/health services
- Military
- Protection services
- Sales
- Technical/IT services
- Transportation/moving
- Veterans USA

**Total Psychographics Options**: 30

---

### 4. Items & Brands (0 categories)

⚠️ **SECÇÃO VAZIA** - Não há categorias disponíveis nesta secção.

**Observação**: Esta secção existe na interface mas não tem filtros implementados. Possivelmente:
- Feature em desenvolvimento
- Requer dados de brand detection que ainda não foram processados
- Relacionado com os 50 items documentados no `data-schema.md` (Ball, Jersey, Shoes, etc.)

**Status**: Não funcional / Placeholder

---

### 5. Behavioral (2 categories, 12 options)

Filtros baseados em comportamentos e preferências de conteúdo.

#### 5.1 Post Category (9 options)
- Breaking News & Announcements
- Entertainment & Celebrity Appearances
- Event & Game Promotions
- Fan Engagement & Memes
- Game Highlights & Player Performances
- Inspirational & Motivational Posts
- Merchandise & Promotions
- Stat Updates & League Standings
- Throwbacks & Historical Moments

#### 5.2 Media Type (3 options)
- carousel
- photo
- reel

**Total Behavioral Options**: 12

---

### 6. Advanced (0 categories)

⚠️ **SECÇÃO VAZIA** - Não há categorias disponíveis nesta secção.

**Observação**: Secção reservada para filtros avançados futuros, possivelmente:
- Combinações complexas de métricas
- Filtros custom/saved
- Análises estatísticas avançadas

**Status**: Não funcional / Placeholder

---

## Summary Statistics

| Section | Categories | Approx. Options | Status |
|---------|-----------|-----------------|---------|
| **Demographics** | 4 | 21 | ✅ Funcional |
| **Location** | 2 | 203 | ✅ Funcional |
| **Psychographics** | 2 | 30 | ✅ Funcional |
| **Items & Brands** | 0 | 0 | ⚠️ Vazio |
| **Behavioral** | 2 | 12 | ✅ Funcional |
| **Advanced** | 0 | 0 | ⚠️ Vazio |
| **TOTAL** | **10** | **~266** | **4/6 funcionais** |

---

## Relação com Data Schema

Cruzamento com `/01-context/data-schema.md`:

### ✅ Filtros Bem Mapeados ao Schema

| Filter Category | Data Schema Field | Entity |
|----------------|-------------------|---------|
| Gender | `author.gender` | Author |
| Age Category | `author.age_category` | Author |
| Ethnicity | `author.ethnicity` | Author |
| Social Status | `author.social_status` | Author |
| Location (Country) | `author.country` | Author |
| Continent | `author.continent` | Author |
| Industry | `author.industry` | Author |
| Post Category | `post.post_category` | Post |
| Media Type | `post.media_type` | Post |

### ⚠️ Schema Fields Não Expostos em Filtros

Campos disponíveis no `data-schema.md` mas **não acessíveis** como filtros:

**Author Entity**:
- `lifestyle` (5 valores documentados) - ✅ **EXISTE em Psychographics > Lifestyle**
- `main_emotion` (25 emoções específicas) - ❌ Não disponível
- `is_verified` (boolean) - ❌ Não disponível
- `follower_range` (7 ranges) - ❌ Não disponível

**Post Entity**:
- `emotions[]` (array de 25 emoções) - ❌ Não disponível
- `call_to_action` (boolean + texto) - ❌ Não disponível
- `items_detected[]` (50 items específicos) - ❌ Não disponível (secção vazia)
- `brands_detected[]` - ❌ Não disponível (secção vazia)

---

## Saved Segments Feature

**Status**: Visível mas vazio ("No saved segments yet")

**Funcionalidade Esperada**:
- Guardar combinações de filtros para reutilização
- Nomenclatura custom de segmentos
- Partilha de segmentos entre utilizadores (?)

**Observação**: Feature implementada na UI mas sem dados. Requer teste de workflow completo:
1. Aplicar filtros
2. Tentar guardar segmento
3. Verificar se segmento aparece em "Saved Segments"

---

## Gap Analysis: Filtros vs Necessidades

### 🔴 Gaps Críticos Identificados

#### 1. Items & Brands (Secção Vazia)
**Impacto**: ALTO
**Problema**: Schema documenta 50 items específicos (Ball, Jersey, Shoes, Sneakers, Sunglasses, Watch, etc.) e 6 categorias de brands (Sportswear, Footwear, Accessories, etc.) mas **não há forma de filtrar audiência por estas características**.

**Use Case Perdido**:
- "Mostre-me comentadores que mencionam Nike"
- "Audiência interessada em sneakers vs jerseys"
- "Perfil de quem comenta posts com bolas vs posts com lifestyle items"

#### 2. Emotional Segmentation (Ausente)
**Impacto**: MÉDIO-ALTO
**Problema**: Schema documenta 25 emoções específicas (Joy, Anger, Surprise, Admiration, etc.) tanto em `author.main_emotion` como `post.emotions[]`, mas não há filtros para segmentar por sentimento.

**Use Case Perdido**:
- "Audiência que expressa mais Joy vs Anger"
- "Commentadores com sentiment negativo predominante"
- "Posts que geram Surprise vs Admiration"

#### 3. Engagement Level (Ausente)
**Impacto**: MÉDIO
**Problema**: Não há filtros baseados em níveis de engagement ou comportamento de interação.

**Use Case Perdido**:
- "Top 10% de commentadores mais ativos"
- "Lurkers vs active participants"
- "Audiência que só dá like vs audiência que comenta"

#### 4. Verification Status (Ausente)
**Impacto**: BAIXO-MÉDIO
**Problema**: Schema documenta `author.is_verified` mas não há filtro.

**Use Case Perdido**:
- "Comentários de contas verificadas"
- "Influencers vs público geral"

---

## Recommendations

### Priority 1: Implementar Items & Brands
- Expor os 50 items e brand categories como filtros
- Permitir filtrar por "contém item X" ou "menciona brand Y"
- Cruzar com Categories (e.g., "Footwear brands mencionadas")

### Priority 2: Adicionar Emotional Filters
- Categoria "Sentiment" em Psychographics
- Opções: 25 emoções específicas do schema
- Permitir filtrar por "dominant emotion" do commentador

### Priority 3: Engagement-Based Filters
- Nova secção "Engagement" ou adicionar em "Behavioral"
- Categorias: Activity Level, Interaction Type, Frequency

### Priority 4: Verificação e Social Proof
- Adicionar em "Demographics" ou "Advanced"
- Filtros: Verified Status, Follower Count Range

---

## UI/UX Observations

### ✅ Pontos Fortes
1. **Estrutura Hierárquica Clara**: Section → Category → Options é intuitivo
2. **Operadores Lógicos**: AND/OR visível e fácil de entender
3. **Contagem de Opções**: Cada categoria mostra quantas opções tem (e.g., "197 options")
4. **Saved Segments Feature**: Espaço reservado para feature útil

### ⚠️ Pontos de Atenção
1. **Secções Vazias Confundem**: "Items & Brands" e "Advanced" aparecem mas não funcionam
2. **Falta Preview**: Não mostra quantos utilizadores match antes de aplicar filtros
3. **Sem Indicação de Popularidade**: Não indica quais opções têm mais dados (e.g., "Male: 60%")
4. **Navegação Repetitiva**: Precisa abrir dropdown → clicar secção → escolher categoria → escolher opções

### 💡 Sugestões de Melhoria
1. **Esconder secções vazias** ou marcar claramente como "Coming Soon"
2. **Adicionar preview de count** ao selecionar filtros (e.g., "~45K users match")
3. **Mostrar distribuição** nas categorias (e.g., "Gender: Male 60% | Female 35% | Other 5%")
4. **Quick Filters**: Atalhos para combinações comuns (e.g., "Young Male Sports Fans")
5. **Filter Templates**: Pre-sets baseados em personas comuns

---

## Technical Notes

### API Mapping (Hypothetical)

Based on filter structure, likely API calls:

```json
POST /api/v1/analytics/community/filter
{
  "operator": "AND",
  "filters": [
    {
      "section": "demographics",
      "category": "gender",
      "values": ["Male", "Female"]
    },
    {
      "section": "location",
      "category": "continent",
      "values": ["Europe"]
    },
    {
      "section": "psychographics",
      "category": "lifestyle",
      "values": ["Active/Sports"]
    }
  ]
}
```

**Response Expected**:
- Filtered author IDs
- Aggregate metrics for filtered segment
- Comparison vs total audience

---

## Related Documentation

- **Portal Audit**: `/03-portal-audit/sitemap.md` (Community page, line 246-442)
- **Data Schema**: `/01-context/data-schema.md` (Author entity fields)
- **API Reference**: `/01-context/api-reference.md` (Community Analytics endpoints)
- **Screenshot**: `filter-location-section.png` (Location section view)

---

**Completion Status**: ✅ Complete tree documented
**Next Steps**: Test saved segments workflow, validate option values against API responses
