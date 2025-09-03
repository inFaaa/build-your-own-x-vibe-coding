# 🤖 Mini-GPT: Build Your First Language Model from Scratch

> Build a "talking" AI with 5 micro-loops (2.5 hours)

## 🎯 What You'll Learn
- **Tokenization**: How to convert text into numbers
- **Attention**: The core mechanism of Transformers
- **Training**: How to make models learn to predict the next word
- **Generation**: Making models generate text

## 🚀 Project Structure
```
mini-gpt/
├── recipes/          # Prompt templates (copy-paste ready)
├── checks/           # Automated test scripts (verify each step)
├── scaffolds/        # Skeleton code (directly runnable)
├── docs/            # Additional documentation
└── vibes.md         # Your build diary
```

## 📚 Learning Path (4 Core Loops)

### Loop 1: Tokenizer (25 minutes)
**Goal**: Convert "hello world" to [123, 456]

**What you'll do**:
1. Copy the prompt from `recipes/01_tokenizer.md`
2. Get an LLM to help you write a simple character-level tokenizer
3. Run `checks/01_tokenizer_test.py` to verify
4. Record in `vibes.md`: What worked? What got stuck?

**Checkpoint**: 
```bash
python checks/01_tokenizer_test.py
# ✅ Should see: "hello" -> [7, 4, 11, 11, 14]
# ✅ Vocab size: 16 (includes special tokens)
```

---

### Loop 2: Mini Transformer (25 minutes)
**Goal**: Implement a 2-layer attention mechanism

**What you'll do**:
1. Start from `scaffolds/02_transformer_skeleton.py`
2. Use `recipes/02_transformer.md` prompt to fill in the code
3. Run `checks/02_transformer_test.py`
4. Record in `vibes.md`

**Checkpoint**:
```bash
python checks/02_transformer_test.py
# ✅ Should see: "Output shape: (2, 10, 100)"
# ✅ Total parameters: 145,764
```

---

### Loop 3: Training Loop (25 minutes)
**Goal**: Make the model learn to predict "hello worl[d]"

**What you'll do**:
1. Use `recipes/03_training.md` to set up the training loop
2. Train on small text for 100 steps
3. Run `checks/03_training_test.py`
4. Record the loss decrease

**Checkpoint**:
```bash
python checks/03_training_test.py
# ✅ Should see: "Loss decreased from 2.85 to 0.03"
# ✅ Model saved to model.pt
```

---

### Loop 4: Text Generation (20 minutes)
**Goal**: Make the model continue sentences

**What you'll do**:
1. Use `recipes/04_generation.md` to implement sampling
2. Given "Once upon", make the model generate 10 words
3. Run `checks/04_generation_test.py`

**Checkpoint**:
```bash
python checks/04_generation_test.py
# ✅ Should see: Generation successful!
# ✅ Example: "Hello" -> "<unk>ello hello hellhe. "
```

---

## 🎯 Final Validation

Run the complete validation to ensure everything works:

```bash
python checks/final_showcase.py
# 🎆 You should see 100% completion! 🎆
```

---

## 🛠️ Environment Setup

```bash
# Minimal installation (only need these)
pip install numpy torch

# Optional: if you want visualization
pip install matplotlib
```

## 💡 What if I Get Stuck?

1. **Every Loop has an escape route**:
   - Check reference implementations in `scaffolds/`
   - Run working versions first, understand then write your own

2. **Prompt not working?**
   - `recipes/` has backup prompts
   - Each prompt has been tested at least 5 times

3. **Check failed?**
   - Every `checks/*.py` has detailed error messages
   - Tells you exactly which line needs fixing

## 🎉 Completion Marker

Run `python checks/final_showcase.py`, you should see:
```
🎆🎆🎆🎆🎆🎆🎆🎆🎆🎆🎆🎆🎆🎆🎆🎆🎆🎆🎆🎆🎆🎆🎆🎆🎆

🎉 Mini-GPT Final Showcase 🎉

✅ Tokenizer: Working normally
✅ Transformer: Forward pass working
✅ Training: Loss decreased from 2.85 to 0.03
✅ Generation: Can generate text

🎉 Congratulations! You have successfully built your own Mini-GPT!
✅ You now understand the core principles of GPT!
```

## 📝 Example vibes.md

```markdown
## Loop 1 - Tokenizer (10:30-10:55)
- Intent: Understand how text becomes numbers
- Friction: Initially didn't understand why <unk> token is needed
- Next: Try BPE tokenizer?

## Loop 2 - Transformer (11:00-11:25)  
- Intent: Implement attention mechanism
- Friction: Matrix dimensions kept mismatching, debugged for 15 minutes
- Next: Visualize attention weights
```

## 🚦 Let's Begin!

```bash
cd mini-gpt
cp recipes/01_tokenizer.md my_prompt.md
# Open your favorite LLM and start Loop 1!
```

---

## 📊 Performance Benchmarks

Our Mini-GPT achieves:
- **Model Size**: 145,764 parameters
- **Training Loss**: 2.85 → 0.03 (97% improvement in 100 steps)  
- **Vocabulary**: 16 characters (including special tokens)
- **Architecture**: 2 layers, 4 attention heads, 64-dimensional embeddings
- **Generation**: Temperature-controlled sampling with multinomial selection

## 🚀 Next Level Challenges

Once you complete the 4 loops, try these extensions:
1. **Larger Data**: Train on Shakespeare or novels
2. **BPE Tokenizer**: Handle words instead of characters
3. **Attention Visualization**: See what the model focuses on
4. **Beam Search**: Better text generation strategy  
5. **Web Interface**: Make it interactive with Gradio/Streamlit

---

*Remember the core of Vibe-Coding: Don't seek perfection, but ensure each loop runs. Get it working first, then optimize!*