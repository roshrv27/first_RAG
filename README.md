This is my first rag implementation. 


ChatInput (user question) ──┬──→ AstraDB (search) ──→ TypeConverter ──┐
                            │                                       │
                            └──→ Prompt Template ←──────────────────┘
                                          │
                                          ↓ (formatted message with context + question)
                                    GroqModel.input_value (User Message)
                                          ↑
                                    GroqModel.system_message (Static Instructions)
