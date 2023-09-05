# OAIS-IM-Ontology

This section ilustrates OAIS-IM ontology that is developed based on OAIS IM reference model [1]. Whole OAIS IM [1] describes metadata that is used for
long term preservation of digital information. Figure 1 shows a part of OAIS IM logical model.  

[<img src="/images/pds-label-uml-model.png" width="550"/>](pds-label-uml-model.png)

*Figure 1. A snapshot of OAIS IM logical model*


Classes from OAIS IM logical model that are shown in Figure 1 are expressed in the OAIS IM KB as concept names. Associations
between classes in from OAIS IM logical model are expressed
as roles names in the OAIS IM KB. Table 1 specifies DL
concept inclusion (CI) axioms including domain and range
restrictions on role names, subsumption relation between
concept names for each term name supported by the OAIS
IM from Figure 1.

[<img src="/images/table-1.png" width="550"/>](table-1.png)

*Table 1. DL Concept Inclusion axioms derived from OAIS Information Model.*

To bring OAIS IM KB alive we use OWL2 [ 2 ] language.
Implemented OAIS IM ontology is available in this Github repository. The AIP concept name is subsumed by AIP concept
name. The AIP as a whole consists of CI as a part. Role name
**composedOf** encodes this part of relation. Domain and range
side restrictions on this role name is shown in Table 1. On
the other hand the CI concept name is also modelled as a whole
that consists of RI concepts as parts. It is encoded using 
**consistOfRI** role name including domain and range restrictions
on this role name (see Table 1). Every instance of AIP is
linked to one or more instances of Package Description (PD)
using **describedBy** role name. Domain and range restrictions
on this role name are also given in Table 1.


#References

[1] CCSDS Secretariat. 2012. Reference model for an open archival information system (OAIS). Technical Report. 
Washington, DC 20546-0001, USA. Online available: https://public.ccsds.org/pubs/650x0m2.pdf

[2] Pascal Hitzler, Markus Krötzsch, Bijan Parsia, Peter F Patel-Schneider, Sebastian Rudolph, et al . 2009. OWL 2 web ontology language primer.
W3C recommendation 27, 1 (2009), 123.
