# SocialIQA_pt
Repo for the Social IQA translation project to Portuguese language for the IA024 class at Unicamp.  

\data           - Folder for source language data in csv format.  
\dataset_en     - Source language dataset folder (en).    
\dataset_pt     - Target language dataset folder (pt).    
\rankings       - Storage for GEMBA translation evaluations.  
\translated     - Storage for temporary translated strings.  

![alt text](https://github.com/fabiograssiotto/SocialIQA_pt/blob/main/images/translation.drawio.png?raw=true)

Workflow notebooks:  
Step I       - read_dataset_en.ipynb       - Initial reading of the source language in JSONL format.  
Step II      - translator_*                - Machine translation using hugging face models.  
Steps III/IV - evaluator_gemba_*.ipynb     - Translation evaluator using a modified GEMBA technique.  
Step V       - publish_dataset_pt.ipynb    - Publishing the target dataset to JSONL format.  

Utility notebooks:  
splitter_training_set.ipynb - Splitter for the training set to handle OpenAI rate limits for the GEMBA evaluation.  
merger_training_set.ipynb   - Merger for the training set post-GEMBA evaluation.  
metrics.ipynb               - Plotter for translation metrics.  

The resulting PT dataset is available at https://huggingface.co/datasets/fabiogr/social_i_qa_pt  
