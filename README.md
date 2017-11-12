# ea-imm
Enterprise Architecture Interoperability Meta-Model Extended by Maturity Models

#Actor.Exist
1.	let lowMaturityProbability : Real = 0.95 in  
2.	let highMaturityProbability : Real =1 in  
3.	let sum:Real= self.maturity->iterate(m:MaturityArea;sum:Real=0|sum+m.level) in  
4.	bernoulli(lowMaturityProbability+((highMaturityProbability-lowMaturityProbability)*(sum/self.maturity->size())))  

#Actor.Distort
1.	let lowMaturityProbability : Real = 0.057 in  
2.	let highMaturityProbability : Real =0.008 in 
3.	let sum:Real= self.maturity->iterate(m:MaturityArea;sum:Real=0|sum+m.level) in  
4.	bernoulli(lowMaturityProbability+((highMaturityProbability-lowMaturityProbability)*(sum/self.maturity->size())))  

#Actor.Drop
1.	let lowMaturityProbability : Real = 0.05 in  
2.	let highMaturityProbability : Real =0 in  
3.	let sum:Real= self.maturity->iterate(m:MaturityArea;sum:Real=0|sum+m.level) in  
4.	bernoulli(lowMaturityProbability+((highMaturityProbability-lowMaturityProbability)*(sum/self.maturity->size())))  

#Actor.isAvailable
1.	let lowMaturityProbability : Real = 0.935 in  
2.	let highMaturityProbability : Real =0.985 in  
3.	let sum:Real= self.maturity->iterate(m:MaturityArea;sum:Real=0|sum+m.level) in  
4.	bernoulli(lowMaturityProbability+((highMaturityProbability-lowMaturityProbability)*(sum/self.maturity->size())))  

#Language.Exist
1.	let lowMaturityProbability : Real = 0.95 in  
2.	let highMaturityProbability : Real =1 in  
3.	let sum:Real= self.maturity->iterate(m:MaturityArea;sum:Real=0|sum+m.level) in  
4.	bernoulli(lowMaturityProbability+((highMaturityProbability-lowMaturityProbability)*(sum/self.maturity->size())))  

#Translation.Exist
1.	let lowMaturityProbability : Real = 0.95 in  
2.	let highMaturityProbability : Real =1 in  
3.	let sum:Real= self.maturity->iterate(m:MaturityArea;sum:Real=0|sum+m.level) in  
4.	bernoulli(lowMaturityProbability+((highMaturityProbability-lowMaturityProbability)*(sum/self.maturity->size())))  

#Translation.Correct
1.	let lowMaturityProbability : Real = 0.949 in  
2.	let highMaturityProbability : Real =0.999 in 
3.	let sum:Real= self.maturity->iterate(m:MaturityArea;sum:Real=0|sum+m.level) in  
4.	bernoulli(lowMaturityProbability+((highMaturityProbability-lowMaturityProbability)*(sum/self.maturity->size())))  

#MPS.Exist
1.	let lowMaturityProbability : Real = 0.949 in  
2.	let highMaturityProbability : Real =0.999 in  
3.	let sum:Real= self.maturity->iterate(m:MaturityArea;sum:Real=0|sum+m.level) in  
4.	bernoulli(lowMaturityProbability+((highMaturityProbability-lowMaturityProbability)*(sum/self.maturity->size())))  


#MPS.Distort
1.	let lowMaturityProbability : Real = 0.049 in  
2.	let highMaturityProbability : Real =0.001 in  
3.	let sum:Real= self.maturity->iterate(m:MaturityArea;sum:Real=0|sum+m.level) in  
4.	bernoulli(lowMaturityProbability+((highMaturityProbability-lowMaturityProbability)*(sum/self.maturity->size())))  

#MPS.Drop
1.	let lowMaturityProbability : Real = 0.05 in  
2.	let highMaturityProbability : Real =0 in  
3.	let sum:Real= self.maturity->iterate(m:MaturityArea;sum:Real=0|sum+m.level) in  
4.	bernoulli(lowMaturityProbability+((highMaturityProbability-lowMaturityProbability)*(sum/self.maturity->size())))  

#MPS.isAvailable
1.	let lowMaturityProbability : Real = 0.935 in  
2.	let highMaturityProbability : Real =0.985 in  
3.	let sum:Real= self.maturity->iterate(m:MaturityArea;sum:Real=0|sum+m.level) in  
4.	bernoulli(lowMaturityProbability+((highMaturityProbability-lowMaturityProbability)*(sum/self.maturity->size())))  

#Address.Exist
1.	let maxProbability : Real = 0.95 in  
2.	let maturityImpact : Real =1 in  
3.	let sum:Real= self.maturity->iterate(m:MaturityArea;sum:Real=0|sum+m.level) in  
4.	bernoulli(lowMaturityProbability+((highMaturityProbability-lowMaturityProbability)*(sum/self.maturity->size())))  

#Example OCL code for injected evidence at MPS.Drop property

1.	if (self.drops_injectEvidence=true) then  
2.	 self.drops_EvidenceToInject  
3.	else  
4.	 if (self.oclIsTypeOf(MPS)) then  
5.	/** MPS class */  
6.	 let lowMaturityProbability : Real = 0.199 in    
7.	 let highMaturityProbability : Real =0.001 in  
8.	 let sum:Real= self.maturityArea->iterate(m:MaturityArea;
9.	 sum:Real=0|sum+m.level) in  
10.	 bernoulli(lowMaturityProbability+((highMaturityProbability-
11.	 lowMaturityProbability)*(sum/self.maturityArea->size())))  
12.	 else  
13.	/** Actor class */  
14.	 let lowMaturityProbability : Real = 0.198 in    
15.	 let highMaturityProbability : Real =0.008 in  
16.	 let sum:Real= self.maturityArea->iterate(m:MaturityArea;
17.	 sum:Real=0|sum+m.level) in  
18.	 bernoulli(lowMaturityProbability+((highMaturityProbability-
19.	 lowMaturityProbability)*(sum/self.maturityArea->size())))  
20.	 endif  
21.	endif  
