This is a LLM-Wiki as proposed by Andrej Karpathy, i am using personally for my journey of learning. It works like a personal compunding knowedge base. 

The following Questions and Answers give a good overview of what is my intention with this LLM-Wiki:

### 1. What problem is this LLM Wiki trying to solve?                                                                                     
                                                                                                                                            
  • Eliminating redundant RAG processing: Traditional document Q&A tools (like ChatGPT file upload or RAG systems) re-read raw document     
  fragments from scratch every time you ask a question. They don't retain learned insights or connections over time.                        
  • Eliminating human maintenance fatigue: Building a personal knowledge base (PKM/Wiki) by hand usually fails because humans get tired of  
  cross-referencing files, updating old summaries, and maintaining indexes.                                                                 
  • The Solution: An LLM incrementally builds and maintains a persistent, structured wiki sitting between you and your source files.        
  Knowledge is processed, connected, and kept current automatically whenever new documents are added or queries are run.                    
  ──────                                                                                                                                    
  ### 2. What are the three layers described in VISION.md?                                                                                  
                                                                                                                                            
  1. Raw Sources (Immutable): Your original files (articles, PDFs, web clips, images, meeting notes). These are read-only and serve as the  
  single source of truth.                                                                                                                   
  2. The Wiki (Persistent Knowledge): A folder of LLM-generated Markdown files containing topic summaries, entity pages, syntheses, and     
  cross-references. You read this layer, and the LLM writes/maintains it.                                                                   
  3. The Schema (Rules & Workflow Config): A master configuration file (e.g. AGENTS.md or schema.md) defining conventions, page templates,  
  file naming rules, and procedures for ingestion, querying, and linting.                                                                   
  ──────                                                                                                                                    
  ### 3. What is the role of Markdown files?                                                                                                
                                                                                                                                            
  • Markdown acts as the universal text interface for the entire system.                                                                    
  • It is human-readable, machine-parsable, version-controllable (via git), portable across operating systems, and natively supported by    
  both LLM agents and tools like Obsidian.                                                                                                  
  ──────                                                                                                                                    
  ### 4. What is the role of Obsidian?                                                                                                      
                                                                                                                                            
  • Obsidian functions as your reader UI ("the IDE") for the knowledge base.                                                                
  • While the LLM acts as the programmer writing to markdown files behind the scenes, you open Obsidian to browse pages, follow interlinked 
  concepts, view graph maps of connected topics, or run metadata queries.                                                                   
  ──────                                                                                                                                    
  ### 5. What is the role of the LLM coding agent?                                                                                          
                                                                                                                                            
  • The LLM acts as the automated wiki maintainer.                                                                                          
  • It performs the heavy lifting: reading raw documents, writing new pages, updating existing entity pages, maintaining cross-links,       
  flagging contradictions, running health checks ("linting"), and saving query insights back into the wiki.                                 
  ──────                                                                                                                                    
  ### 6. Why are index.md and log.md important?                                                                                             
                                                                                                                                            
  • index.md (Content Map): A organized catalog of all pages in the wiki with links and one-line summaries. The LLM checks index.md first   
  during a query to quickly identify relevant files without needing expensive vector database infrastructure.                               
  • log.md (Timeline & History): An append-only, chronological log tracking what happened (ingests, queries, lint runs). It gives both you  
  and the LLM an audit trail of how the wiki has evolved.                                                                                   
  ──────                                                                                                                                    
  ### 7. How does knowledge compound in this system?                                                                                        
                                                                                                                                            
  Knowledge compounds in two key ways:                                                                                                      
                                                                                                                                            
  1. Incremental Ingestion: Adding a single source updates multiple existing concept pages, refines summaries, flags conflicts with past    
  claims, and establishes cross-links.                                                                                                      
  2. Filing Queries Back: When you ask the LLM to synthesize an answer or run a complex comparison, that answer is saved back into the wiki 
  as a new page. Your past questions become permanent knowledge assets for future queries.                                                  
  ──────                                                                                                                                    
  ### 8. What decisions does VISION.md intentionally leave open?                                                                            
                                                                                                                                            
  VISION.md is a high-level design blueprint, leaving specific implementation details up to you and your LLM agent to decide together:      
                                                                                                                                            
  • Directory structure: Exact layout of folders (e.g., raw/, wiki/, assets/).                                                              
  • Schema details: Exact frontmatter properties, tag structures, and page formats.                                                         
  • Search tooling: Whether to rely solely on index.md, simple text search, or local CLI search engines (like qmd).                         
  • Workflows: Interactive single-source processing vs. automated batch ingestion.                                                          
  • Plugins & Extra Formats: Use of slide decks (Marp), metadata queries (Dataview), or local image downloads.
