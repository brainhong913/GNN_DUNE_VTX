# GNN_DUNE_VTX
A documentation on how to generate samples and use of the GNN for vtx reco
All the source code is available. Code tested with version 10_04_06
# Local Use
Before start, read https://larsoft.org/to-set-up-and-run-larsoft/ to know how to setup your own larsoft. 
Please setup duneana and larpandoracontent.
After setting up, you shall see there's srcs file
You just need to replace the srcs file with the one in github. 
Local use example:
For generate .data graph files:

lar -c atm-training-extract.fcl -s detsim.root

For generate subrun-event-id table
lar -c eid.fcl -s detsim.root                   
To generate root file for truth_eid


# Submit jobs
Please read https://gitlab.in2p3.fr/pgranger/atmo_gen
This is a  using the offical production.
You will likely need the larsoft_graph_V1_2025.tar.gz and the yaml
- name:         Reco to generate graph file for U,V,W
- name:         Subrunlist to generate extra root file to fix the subrun event id problem
You will likely to also need   # - name:           AnaTree to generate anatree


So if you follow below, you shall produced :
1. Anatree for all of the files
2. graph data, as .data
3. eid fix file, which is a root file


