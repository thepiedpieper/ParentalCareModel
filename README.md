# A. Details of the model
## 1) Introduction:
As long as female preference acts on a population containing diﬀerent male types, polymorphism persists indeﬁnitely. They also state that the rarer phenotypes become more common, which
is outside the scope of this model, because of dynamic selection of quality thresholds. However, to test
the ﬁrst part of the claim, we decided to test whether lower quality males resorted to faring suboptimally
using the same strategies as the higher qualoty males (here, the rarer phenotype) or whether they try to
maximise their ﬁtness using some other strategy which would be suboptimal for the high quality males,
given their ecological conditions.
Quoting [2], the coevolution of parental care and mating strategies hinder mutual mate choice if the re-
duced care provided by one parent can be compensated for by the other sex, but actually promotes it if
the survival of oﬀspring is dependent on both parents. In this model, we sought to look at the evolution
of biparental care from female care in polygynous populations, and whether there is a diﬀerence in the
amount of parental care oﬀered by lower quality males on an average, mandating that mutual mate choice
exists, and biparental care provides a beneﬁt in terms of increased survival of oﬀspring. This system of
parental care is termed synergistic care, where two parents together can produce more oﬀsprings than the
lone parent.
In our model, males and females both have qualities denoted by a variable q. The value of q for male shas
a dual meaning. High quality males have a higher quality of ornaments, and they are also more likely to
get selected for by females. Similarly, in females, a higher value of q signiﬁes more fecundity, and a higher
chance of getting selected by males in the same territory as hers.
The model imitates a mxn spatial grid, where a polygynous population is initiated by randomly spread-
ing 2N individuals randomly across the grid. The sex is chosen randomly, while ensuring that the sex ratio
is 1:1. Each square in this matrix like grid is considered to be a territory like place.


_Some of the basic assumptions of the model are as follows:_

1. The species is annual, with a lifespan of 1 year on average, with non overlapping generations.
2. The females are territorial, with each of them having a ﬁxed territory, which they do not move out
of. Each territory corresponds to a single square in the matrix. Territory size does not depend on
the quality of females, and instead is the same for all females, for simplicity.
3. Males are free to move out of their initial positions, and they can roam randomly over the territory,
however only at a ﬁxed dispersal rate. To keep things realistic, we assume that the male, from its
current position (a single square), can scan the surrounding 20 squares to see if there is a female
territory in any of these.
4. A mating event happens only when the male is in the female’s territory, and is chosen by the female.
5. We have included mutual mate choice instead of the predominant female choice model used for
polygyny.
The model aims to see if high quality and low quality males adopt diﬀerent mating strategies in order to
maximise their ﬁtness, and if low quality males evolve to provide more parental care than high quality
males as compensation for their low quality. In this model, we assume, spending time with a gravid part-
ner as a measure of providing parental care, which results in ﬁtness beneﬁts, in the form of more living
oﬀsprings.


## 2) The Model:
1. Initialisation of the population:A population of 2N individuals is initiated on the mxn grid, where the sex of individuals is cho-
sen randomly, keeping the sex ratio 1:1. Males are assigned qualities ranging from 0 to 1, which are
random values drawn from a beta distribution with a mode of around 0.3, which ensures that high
quality males are comparatively rare in the population, as we would expect in a realistic scenario.
Females are also assigned qualities the same way, with the same mode of around 0.3. All males and
females initially have a ﬁtness of 0.
2. Mating:
For simplicity, we look only at the breeding season of the species, and discard other non-repro-
duction related activities as they do not have any signiﬁcance in the model. We consider an average
breeding season of 6 days. We also mandate the all non-gravid individuals have to make a decision
every day of the breeding season. For the males, this involves taking a decision on whether to stay
with its recently mated gravid partner, or seek out a more desirable female in the vicinity. For non-
gravid females, this involves making a decision on which male to mate with, provided that the males
in question are in her territory. Females once mated, becomegravid for a period of the subsequent
14 days, and is not available for further matings.
3. Male-Mate choice:
Males in the population choose female mates based on their desirability. Desirability of a par-
ticular female is calculated based on the female’s quality, and the negative competition cost that the
male faces from other males courting the same female. If the desirability of a particular femae in the
immediate vicinity (in this case, the surrounding 20 squares), exceeds the ﬁtness beneﬁt the male
would receive by staying with its gravid partner, it moves to the territory of the desirable female, in
hopes of initiating another mating. Males make this decision everyday, and receive a ﬁtness beneﬁt
in the form of increased survival of oﬀsprings if it stays for the entire 14 days that its partner is
gravid. For ease of reference, we shall be calling this beneﬁt, the monogamy beneﬁt .
4. Female Mate Choice:
In the basic version of the model, the females simply choose the best quality male available
in her territory. We assume higher quality in females translates to higher fecundity, hence, higher
quality females would lay a larger clutch. In other words, the size of the clutch is directly propor-
tional to the females quality. Once the clutch is laid, the sex of the oﬀspring is randomly chosen,
while maintaining the sex ratio of 1:1. The quality of each of the oﬀspring is drawn from a normal
distribution centred around the mean of the qualities of its parents.
5. Maturation of juveniles
Oﬀsprings become juveniles at the end of the breeding season, and the previous generation dies.
At the end of each breeding season, we allot a ﬁxed time for the oﬀsprings to mature, during which
they spread out of their mother’s territory to neighbouring squares, in order to avoid clumping, and
high rates of inbreeding.
The simulation is run for 50 generations in order to capture the average decisions of high and low
quality males.
## 3) Hypotheses:
We put forward the following hypotheses, based on the parameter we took for the model:
- Sex ratio
We hypothesised that the time the lower quality males decide to spend with their mated partner would
depend on the number of surrounding males. We expected that in case of a male biased sex ratio, because
of more male counterparts, lower quality males would spend more time with their gravid partner because
of lower chances of securing further matings. This is also based on empirical evidence from the male-bi-
ased dunnock populations, where lower quality males are seen to provide more parental care as compared
to their higher quality counter parts.
- Length of the breeding season
We hypothesised that as the length of the breeding season increases, the cost of staying with a female
for the same number of days would be much less in case of a longer breeding season as compared to a
shorter one.
- Density of individuals.
On a high density grid, all individuals adopt Stay as a form of probable mate guarding - fierce competition (?)
In low density conditions (20 individuals in a 20x20 grid), strategies split - low density seems to be essential.
- Migration rate of the oﬀsprings
As mentioned earlier, the juveniles disperse from their mother’s territory to reduce chances of high in-
breeding. We hypothesised that lower quality males would be more likely to come across lower quality
females in case of lower migration rates, due to clumping eﬀects. The beneﬁts of staying would therefore
be more signiﬁcant as compared to mating with another low quality female. Hence parental care provided
by low quality males should decrease with higher migration rates.
- Proportion of high quality females in the population
We hypothesised that the availability of more high quality females around can push lower quality males
to make more use of the polygyny potential of the environment. This is because, the beneﬁt of mating a
higher quality male and having a large clutch, would exceed the beneﬁt of staying with the same female.
Indeed, we ﬁnd that the pattern dissolves.

We can say that in our model, the evolution of biparental care can be expected under most
parametric conditions, given that mutual mate choice exists.This has been true for all the parameters
tested. While that is encouraging this also led us to test for a new hypothesis - we sought to ﬁnd out
whether there was any diﬀerence in the capability of males of diﬀerent qualities in a polygynous popu-
lation for exploiting the polygamy potential that their environment provided. INteretingly as far as the
results go, we do see an apparent diﬀerence in how frequently males of the two qualities decide to invest
in parental care and thus pay a “breeding cost” which aﬀects their future matings and ﬁtnesses. As per
Trivers (1972), a decision to invest in parental care also translates to signalling induced mortality during
mating. In the model of synergistic parental care that we tested, we can conclude that inspite of frequent
mate interactions, both higher and lower quality males can exercise mate choice by deciding to not invest
in polygyny.
