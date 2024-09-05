# snakes
Improving existing _de novo_ peptide sequencing models.

Snakes pose a significant danger in Senegal, where encounters with venomous species can lead to severe injury or even death. The diversity and potency of snake venoms in the region present a major public health challenge, with traditional methods of antivenom production often falling short due to the unique and complex nature of these venoms. This is where [tandem mass spectrometry](https://en.wikipedia.org/wiki/Tandem_mass_spectrometry) combined with [_de novo_ peptide sequencing](https://en.wikipedia.org/wiki/De_novo_peptide_sequencing) could potentially play a role.

_De novo_ peptide sequencing involves determining the amino acid sequence of peptides from a mass spectrum without prior knowledge of the protein sequence, potentially making it a tool in the fight against snake bites. Unlike traditional database search methods, which rely on existing sequence databases and often fail when encountering novel or highly variable venom components, _de novo_ sequencing provides an unbiased and comprehensive analysis of venom peptides. This approach could potentially allow for the identification of new and unique venom peptides, which is crucial for the development of effective and specific antivenoms.

By leveraging mass spectrometry with _de novo_ peptide sequencing, researchers could potentially create tailored antivenoms that are more effective against the diverse snake venom profiles found in Senegal. If successful, This may have the potential not only to improve the chances of survival for snakebite victims but also to enhance the overall public health response to snakebite emergencies. We believe that the ability to rapidly and accurately sequence venom peptides could represent a significant advancement in our efforts to combat the dangers posed by snakes in Senegal and beyond.

## The Task: recalibrating model predictions

How can we help? In this hackathon we will be improving existing _de novo_ peptide sequencing models. Specifically, we will be looking into recalibration and filtering! Rather than training a large _de novo_ sequencing model from scratch, we will focus on using various techniques to improve the area under the curve (AUC) for the precision-recall graph. Due to high noise, our models are often not super well calibrated.

InstaDeep has developed a transformer-based _de novo_ peptide sequencing model **InstaNovo** [[preprint](https://www.biorxiv.org/content/10.1101/2023.08.30.555055v3)][[code](https://github.com/instadeepai/InstaNovo)]. 
We will provide you with the inputs AND outputs of InstaNovo along with some additional metadata (eg. retention time). The InstaNovo outputs includes the top 5 beam predictions along with their model confidences.
Your task is to use these inputs and metadata to re-calibrate the confidence measurements and filter out any false positives in order to maximise the AUC!
