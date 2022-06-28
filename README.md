# Jet-V0 analysis in pPb at 8.16 TeV

This folder contain relevant information about the data processing of V0s in pPb at 8.16 TeV for the dataset collected by CMS in the Run 2 at November/December of 2016.

## Analysis steps

V0 skim production -> tree production -> matching V0 trees with forest -> produce histograms -> run macros to obtain observables

## CMSSW setup (at LXPLUS)
```
cmsrel CMSSW_8_0_28
cd CMSSW_8_0_28/src
cmsenv
git clone git@github.com:davidlw/VertexCompositeAnalysis.git
scram b -j 10
```

The skim production step is included in the folder VertexCompositeProducer. 
- for V0s:
  - code: https://github.com/davidlw/VertexCompositeAnalysis/blob/master/VertexCompositeProducer/src/V0Fitter.cc
  - configuration: https://github.com/davidlw/VertexCompositeAnalysis/blob/master/VertexCompositeProducer/test/pPbSkim2016_V0_cfg.py
  - selections: https://github.com/davidlw/VertexCompositeAnalysis/blob/master/VertexCompositeProducer/python/generalV0Candidates_cfi.py

For a test, you can run the VertexCompositeProducer/test/pPbSkim2016_V0_cfg.py using:
```
cmsRun pPbSkim2016_V0_cfg.py
```
  
## Skim processing
### MC Simulations with PYTHIA
...
