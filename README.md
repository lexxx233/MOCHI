# MOCHI (Mindful Optimized Companion for Human Interaction)

The Goal of this project is to make a long term LLM companion that

1. Mochi is an LLM-based companion
2. Mochi actively build relationship
3. Mochi has memory
4. Your Mochi is private
5. Your Mochi's personality is unique

---
config:
  layout: elk
---
flowchart TD
 subgraph Emotions["🌊 Multi-Temporal Emotion System"]
        STE["⚡ Short-term<br>1-5 interactions<br>Decay: 0.3"]
        MTE["🌀 Medium-term<br>Session level<br>Decay: 0.1"]
        LTE["🏛️ Long-term<br>Cross-session<br>Decay: 0.02"]
        CEV["📊 Composite Emotion Vector"]
        EmotionState(("Emotion State"))
  end
 subgraph SpeechEvolution["🗣️ Speech Pattern Evolution"]
        EP["🎲 Exploration Probability"]
        UF["📈 User Feedback"]
        PM["🧬 Pattern Mutation"]
        R["🎖️ Reinforcement"]
        SpeechParams["Speech Parameters"]
  end
 subgraph SleepSystem["🌙 Sleep-Based Memory Consolidation"]
        LightSleep["🌅 Light Sleep"]
        PreSleep["😴 Pre-Sleep Reflection"]
        DeepSleep["🌌 Deep Sleep"]
        REMSleep["💭 REM Sleep"]
        Consolidation["🧠 Memory Consolidation"]
  end
 subgraph MemorySystem["💾 Memory & Personality Persistence"]
        WM["📝 Working Memory<br>Current session context"]
        SC["📋 Session Context<br>Conversation patterns"]
        LTI["🎭 Long-term Identity<br>Core personality traits"]
  end
 subgraph LearningLoop["🔄 Continuous Learning Loop"]
        CL["🎯 Continuous Learning:<br>Response → Feedback → Evolution → Consolidation"]
  end
 subgraph Innovation["✨ Key Innovation"]
        MultiLayer["🎯 Multi-layered Response Generation<br>Every response = Current Emotions +<br>Speech Patterns + Working Memory +<br>Session Context + Long-term Identity"]
  end
    User["👤 User Interaction"] --> RT["🧠 Real-time Processing"]
    RT --> STE & SP["💬 Speech Pattern Selection"] & RG["🎯 Response Generation"]
    STE --> CEV
    MTE --> CEV
    LTE --> CEV
    CEV -- "Valence [-1,1]<br>Arousal [0,1]<br>Dominance [0,1]<br>Curiosity [0,1]<br>Attachment [0,1]" --> EmotionState
    UF --> EP
    EP --> PM
    PM --> R
    EP -- Higher satisfaction<br>→ Lower exploration<br>(but never 0%) --> SpeechParams
    EmotionState --> RG
    SpeechParams --> RG
    WM --> RG
    SC --> RG
    LTI --> RG
    RG -- Unique Response --> Response["📤 Generated Response"]
    Response --> UF
    Response -- Session End --> PreSleep
    PreSleep -- "Emotional afterglow<br>Self-assessment<br>Future anticipation" --> LightSleep
    LightSleep -- Memory ranking<br>Pattern success<br>Emotion peaks --> DeepSleep
    DeepSleep -- "Long-term encoding<br>Emotion regulation<br>Core identity update" --> REMSleep
    REMSleep -- Pattern variations<br>Scenario simulation<br>Creative recombination --> Consolidation
    Consolidation --> WM & SC & LTI
    MemorySystem --> CL
    CL -- Personality Evolution --> Emotions
    CL -- Speech Development --> SpeechEvolution
    LTI -.-> MTE & LTE
    SC -.-> SP
     STE:::emotionClass
     MTE:::emotionClass
     LTE:::emotionClass
     CEV:::emotionClass
     EmotionState:::emotionClass
     EP:::speechClass
     UF:::speechClass
     PM:::speechClass
     R:::speechClass
     SpeechParams:::speechClass
     LightSleep:::sleepClass
     PreSleep:::sleepClass
     DeepSleep:::sleepClass
     REMSleep:::sleepClass
     Consolidation:::sleepClass
     WM:::memoryClass
     SC:::memoryClass
     LTI:::memoryClass
     MultiLayer:::innovationClass
     User:::userClass
     RT:::userClass
     RG:::responseClass
     Response:::responseClass
    classDef userClass fill:#3498db,stroke:#2980b9,stroke-width:3px,color:#fff
    classDef emotionClass fill:#f39c12,stroke:#e67e22,stroke-width:2px,color:#fff
    classDef speechClass fill:#27ae60,stroke:#229954,stroke-width:2px,color:#fff
    classDef sleepClass fill:#e67e22,stroke:#d35400,stroke-width:2px,color:#fff
    classDef memoryClass fill:#3498db,stroke:#2980b9,stroke-width:2px,color:#fff
    classDef responseClass fill:#9b59b6,stroke:#8e44ad,stroke-width:3px,color:#fff
    classDef innovationClass fill:#f1c40f,stroke:#f39c12,stroke-width:2px,color:#000

