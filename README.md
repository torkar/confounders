# Confounders
Replication package for study on confounders.

## TODO

Start with,

why experiments are the gold standard
explain confounders
point at the challenge MSR studies have if they don't take causality into account

Next introduce causal analysis a la Perl / Hernan et al.
elemental constructs
point to how not including a collider is a good thing
point to the danger of confounders
latent (unobserved) variables can be confounders... indicated what we can do!

Simple example of confounders and how they affect the direct effect w/ sim data

Advanced example of confounders from Shepperd, first with sim data then with empirical data.

Show how we can analyze possible effect of unobserved confounders.


Provide checklist with what one always should do with observational studies

http://dagitty.net/mP8mw_j

U1 -> n/a
U2 -> n/a
U3 -> iff exists need to condition on L
U4 -> n/a
U5 -> n/a
U6 -> omitted variable bias
U7 -> omitted variable bias
U8 -> iff exists need to condition on PL
U9 -> omitted variable bias
[BA <- U10 -> PT] -> iff exists need to condition on PT
[BA <- U11 -> S] -> iff exists need to condition on S
[BA <- U12 -> TS] -> iff exists need to condition on TS

Hence, a full set should be {P,A,O,H,PL,L,PT,S,TS} (conditioning on PL,L,PT,S,TS would take care of unknown confunders U3 and U8, and U10-U12), but we still have a problem with U6,U7,U9.

dag {
bb="0,0,1,1"
BA [exposure,pos="0.452,0.130"]
H [adjusted,pos="0.657,0.248"]
L [adjusted,pos="0.246,0.413"]
O [adjusted,pos="0.244,0.245"]
P [outcome,pos="0.454,0.449"]
PL [adjusted,pos="0.658,0.424"]
PT [adjusted,pos="0.344,0.700"]
S [adjusted,pos="0.540,0.709"]
TS [adjusted,pos="0.634,0.623"]
U1 [latent,pos="0.577,0.144"]
U2 [latent,pos="0.327,0.145"]
U3 [latent,pos="0.220,0.329"]
U4 [latent,pos="0.338,0.453"]
U5 [latent,pos="0.569,0.460"]
U6 [latent,pos="0.317,0.349"]
U7 [latent,pos="0.429,0.278"]
U8 [latent,pos="0.682,0.335"]
U9 [latent,pos="0.584,0.354"]
BA -> H
BA -> P
H -> P
H -> PL
L -> P
O -> BA
O -> L
O -> P
PL -> P
PT -> P
S -> P
S -> TS
TS -> P
}

