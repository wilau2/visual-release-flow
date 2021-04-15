# goto-visual-flow


                               Pull request checklist                                                                                                                                   
                                 Pull request review                                                                                                                                    
                                  Squash and merge                                                                                                                                      
                             ┌──────────────────────────┐                     ┌───────────────git checkout -b──────────────┐┌─────────────git checkout -b─────────────┐                 
                             │                          │                     │                                            ││                                         │                 
                             │                          │                     │                                            ▼│                                         ▼                 
                  ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─               │          ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─                      ─ ─ ─ ─ ─ ─ ┴ ─ ─ ─ ─ ─                    ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─      
                       feature branch                   │               develop branch                             release/nov1st2020                         release/nov2nd2020        
                │                         │             │        │                         │                  │                         │                │                         │    
                   ─────────────────────                │           ─────────────────────                        ─────────────────────                      ─────────────────────       
                │ │                     │ │             │        │ │                     │ │                  │ │                     │ │                │ │                     │ │    
                  │   feat: feature A   ├ ─ ─ ─ ─ ─ ─ ─ ┴──────────┼▶  feat: feature A   ├──────────────────────┼▶  feat: feature A   ├────────────────────┼▶  feat: feature A   │      
                │ │                     │ │                      │ │                     │ │                  │ │                     │ │                │ │                     │ │    
                   ─────────────────────                            ─────────────────────                        ─────────────────────                      ─────────────────────       
                │                         │                      │                         │                  │                         │                │                         │    
                 ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─                                                                     ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─                                                
                                                                 │                         │                               │                             │                         │    
                  ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─                                                                                  │                                                            
                       feature branch                            │                         │                               │                             │                         │    
                │                         │                                                                                │                                                            
                   ─────────────────────                         │  ─────────────────────  │                               │                             │                         │    
                │ │                     │ │                        │                     │                                 │                                                            
                  │   feat: feature B   │────────────────────────┼─┼▶  feat: feature B   │ │                               │                             │                         │    
                │ │                     │ │                        │                     │                                 │                                                            
                   ─────────────────────                         │  ─────────────────────  │                               │                             │                         │    
                │                         │                                                                                │                                                            
                 ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─                       │                         │                               │                             │                         │    
                                                                                                                           │                                                            
                  ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─                        │                         │                               │                             │                         │    
                         fix branch                                                                                        │                                                            
                │                         │                      │                         │                               │                             │                         │    
                   ─────────────────────                            ─────────────────────                                  │                                ─────────────────────       
                │ │                     │ │                      │ │                     │ │                               │                             │ │                     │ │    
             ┌ ▷  │    fix: feature A   │──────────────────────────┼▶   fix: feature A   ├──────────────────────────git cherry-pick────────────────────────┼▶   fix: feature A   │      
                │ │                     │ │                      │ │                     │ │                               │                             │ │                     │ │    
             │     ─────────────────────                            ─────────────────────                                  │                                ─────────────────────       
                │                         │                      │                         │                               │                               ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─      
             │   ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─                                                                                 │                                          │                 
                                                                 │                         │                               │                                          │                 
             │    ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─                                                                                  │                                          │                 
                       feature branch                            │                         │                               │                                          │                 
             │  │                         │                                                                                │                                          │                 
                   ─────────────────────                         │  ─────────────────────  │                               │                                          │                 
             │  │ │                     │ │                        │                     │                                 │                                          │                 
                  │   feat: feature C   ├────────────────────────┼─┼▶  feat: feature C   │ │                               │                                          │                 
             │  │ │                     │ │                        │                     │                                 │                                          │                 
                   ─────────────────────                         │  ─────────────────────  │                               │                                          │                 
             │  │                         │                                                                                │                                          │                 
                 ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─                       │                         │                               │                                          │                 
             │                                                                                                             │                                          │                 
                  ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─                        │                         │                               │                                          │                 
             │           fix branch                                                                              git push --set-upstream                    git push --set-upstream     
                │                         │                      │                         │                    origin release/nov1st2020                  origin release/nov2nd2020    
             │     ─────────────────────                            ─────────────────────                                  │                                          │                 
                │ │                     │ │                      │ │                     │ │                               │                                          │                 
             │    │  fix: feat A again  ├ ─ ─ ─ ─ ─ ─ ─┌──────────▶│▶ fix: feat A again  │                                 │                                          │                 
                │ │                     │ │            │         │ │                     │ │                               │                                          │                 
             │     ─────────────────────               │            ─────────────────────                                  │                                          │                 
                │                         │            │         │                         │                               │                                          │                 
             │   ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─             │          ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─                                │                                          │                 
                             │                         │                      │                                            │                                          │                 
             │                                         │                      │                                            │                                          │                 
                             │                         │                      │                                            │                                          │                 
             │                                         │                      │                                            │                                          │                 
                             ▼                         │                      ▼                                            │                                          │                 
             │  ┌─────────────────────────┐            │         ┌─────────────────────────┐                               │                                          │                 
                │    Manually create an   │            │         │  Jenkins automatically  │                               │                                          │                 
             │  │     APK and IPA from    │            │         │   creates an internal   │                               ▼                                          ▼                 
                │    your branch using    │            │      ┌──│release every week night │                          ┌───────────────────────────────────────────────────┐             
             │  │         jenkins         │            │      │  │                         │                          │                                                   │             
                └─────────────────────────┘            │      │  └─────────────────────────┘                          │      Jenkins automatically creates a release      │             
             │               │                         │      │               ▲                                       │   candidate on playstore and itunesconnect when   │             
                             │                         │      │               │                                       │     a release/* branch is pushed on the origin    │             
             │               └─────────────────────────┘      └───────────────┘                                       │                                                   │             
                                 QA/PO can test fix            Every morning, QA/PO can                               └───────────────────────────────────────────────────┘             
             │                   or feature from the            validate what have been                                    │                                           │                
                                   generated build             merged to develop the day                                   │                                           │                
             │                   before it is merged                    before                                             │                                    QA validate fix         
                                     to develop                                                                 QA full regression tests               QA regression on impacted feature
             │                                                                                                             │                                           │                
                                                                                                                           │                                           │                
             │                                                                                                             ▼                                           ▼                
                                                                                                                       ┌──────────────────────────────────────────────────┐             
             │                                                                                                         │                                                  │             
                                                                                                                       │         Trigger manually the production          │             
             │                                                                                                         │                rollout on Jenkins                │             
                                                                                                                       │                                                  │             
             │                                                                                                         │                                                  │             
                                                                                                                       └──────────────────────────────────────────────────┘             
             │                                                                                                                                   │                                      
                                                                                                                                   ┌─────────────┴─────────────┐                        
             │                                                                                                                     ▼                           ▼                        
                                                                                                                       ┌──────────────────────┐    ┌──────────────────────┐             
             │                                                                                                         │      PlayStore       │    │    iTunesConnect     │             
                                                                                                                       │                      │    │                      │             
             │                                                                                                         └──────────────────────┘    └──────────────────────┘             
                                                                                                                                   │                           │                        
             │                                                                                                                     └─────────────┬─────────────┘                        
                                                                                                                                                 ▼                                      
             │                                ┌────────────────────────────────────┐                                   ┌──────────────────────────────────────────────────┐             
                                              │                                    │                                   │                                                  │             
             │                                │    Halt production rollout need    │                                   │           Jenkins syncs up Play Store's          │             
              ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ┤           fix: feature A           │─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─│        rollout with iTunesConnect's phased       │             
                                              │                                    │                                   │                      release                     │             
                                              └────────────────────────────────────┘                                   │                                                  │             
                                                                                                                       └──────────────────────────────────────────────────┘             
                                                                                                                                                 │                                      
                                                                                                                                                 │                                      
                                                                                                                                                 ▼                                      
                                                                                                                       ┌┬───────────────────────────────────────────────┬┐              
                                                                                                                       ││           When rollout reaches 100%           ││              
                                                                                                                       │└───────────────────────────────────────────────┘│              
                                                                                                                       │        Jenkins updates the Deploy tickets       │              
                                                                                                                       │       and Jira's releases to consider them      │              
                                                                                                                       │                   as released                   │              
                                                                                                                       │                                                 │              
                                                                                                                       │       Jenkins moves tickets that has been       │              
                                                                                                                       │       assigned to the version we have just      │              
                                                                                                                       │                     released                    │              
                                                                                                                       │                                                 │              
                                                                                                                       └─────────────────────────────────────────────────┘             
