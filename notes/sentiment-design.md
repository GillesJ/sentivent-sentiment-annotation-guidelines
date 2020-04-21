CHOICES:

- Implicit aspect vs explicit aspect: aspect expressions should explicitly belong to 
e.g. ``[The weight](WEIGHT explicit) of the phone is [too heavy[(polar expression) and [the price](PRICE explicit) [too high](polar expression).'' vs. ``The phone is [too [heavy](<-implicit WEIGHT)](polar expression) and [too [expensive](<-implicit PRICE)](polar expression)''
TODO cf implicit aspect survey for overview

- Required TARGET:

TERMINOLOGY:
- SentiFM: polar expression = any word span containing implicit or explicit sentiment INCLUDING EVENTS WITH IMPLICIT SENTIMENT

## SentiFM annotations: 
- Polar expression annotation: 3 attributes
    - Type: continuum from objective to subjective: DO NOT DO THIS: Too difficult will slow annotation down: Make binary distinction
    - CONFIDENCE SCORE: we will not
    - Insubstantiality: sentiment is not real, or denied by context: useful
    - Causativity: polar expressions refer to a positive or negative effect being exerted on a target entity by another entity.
    
- Modifiers: DO NOT ANNOTATE TO INVOLVED partially replace by Factuality: negated/insubstantial and Modal:other
- Source entity and source expression: TOO INVOLVED scrap or simplify this by only annotating source not the linking source expression
- Target and sentiment polarity: 
    Multiple targets possible
    2 attributes marked on target level > good idea!!!
    - Polarity: positive, negative, other(=emotions such as surprise), unknown=ambiguous based on perspective -> good!
    - Intensity: low, medium, high: scrap this

- Causativity: SentiFM annotates polar expressions with an attribute is\_causative if the polar expression indicates a negative or positive effect is exerted on the sentiment target. They additionally annotate the causing entity with a "cause" relation to the polar expression. We deem this to complicated for our annotation scheme. DO NOT ANNOTATE

## EventDNA annotations:
Consider each sentence in turn:
- Minimal wordspan rule: Good take this over, No insane restrictions
- Step 1: Look at event and entity spans and determine prototypical (implicit) polarity
- Step 2: Annotate minimal wordspan of polar expression related to the event >
- Step 3: Determine the same for entities >
NB: no difference in the way we treat events and entities in annotating sentiment
NB: clean interface off coreference links etc. > Need preprocessing of data?
- Step 4: Other polar expressions in text + target.
-> Step 4 needs to be very clear and as unified as possible with

Conclusion:
START with EVENTDNA annotations: go step by step: what if polar opinion expression outside of event: do that > slightly different concepts of event that need to be unified as much as possible 

DEVELOPMENT STEPS: 
Determine which attributes on event and entities to annotate
- If polarity on event or entity = implicit
=> QUESTION: DOES IT HAPPEN THAT WITH THESE IMPLICIT TYPES A POLAR EXPRESSION IS MENTIONED?
=> QUESTION: ARE OtherModality and Negated on Events the same attributes: NOT important > make new features for these
- 
- 
Next determine properties of polar expressions

Options: Event itself is has implicit sentiment > as attribute on 
Otherwise: polar expression with sentiment associated > as attribute 

OPEN QUESTIONS:
- Do we annotate polar expression outside the event typology, i.e. do we annotate any polar expression as in SentiFM. SentiFM does not have a unified concept of an event-sentiment relation (annotated separately)
  - If yes: We capture ALL implicit sentiment expressions or ALL polar facts even the ones that are not connected to our event typology.
    - Approach: We still start annotation steps with annotating implicit sentiment on Events/entities, but add steps to annotate all polar expressions INCLUDING IMPLICIT POLAR FACTS outside of event/entities. As of now we include only 
    - Advantage: Not limited to event/entity annotations. 
    - Disadvantage: Annotation difficulty increases significantly because we have to explain the difference between implicit and explicit sentiment plus we have to define implicit sentiment which is more difficult to annotate than explicit sentiment expressions. 
  - If NO: We define implicit sentiment as existing only on event/entity mentions.
    - Approach: Cf. current chart: Only explicit sentiment is annotated outside of mentions.
    - Advantage: Easier annotation, no need to explain and annotate implicit polar expression separately. Annotations more in line with EventDNA which does not handle implicit sentiment as its own category.
    - Disadvantage: Miss a lot of potential polar facts. However not linked to events. Only partially compatible with SentiFM dataset.
- Do we really need to annotate prototypical sentiment on entities?
Does not seem to have a lot of polarity on them > mostly neutral association at best, or it would require a lot of investor and domain knowledge of the market to assign a sentiment to a company.
> Ask Orphee and Cynthia what they think of this. Have they done trails or do they expect this to be useful in downstream tasks???
- 