# positional-encoding
This repository is my attempt to truly understand positional encodings used in Transformer models — not just use them as a black box.

Instead of jumping straight into frameworks, I build positional encodings step by step using NumPy, visualize them, and connect the math with intuition.

⸻

Why Positional Encoding?

Transformers do not understand word order by default.

For example:

“I love you”
“You love I”

Both sentences contain the same words, but their meanings are different.
Self-attention alone cannot distinguish this.

Positional Encoding solves this by injecting information about where each token appears in a sequence.

⸻

 What This Notebook Covers
	•	What positions mean in Transformers
	•	Why order information is required
	•	How sinusoidal positional encodings are constructed
	•	Why sine and cosine are used
	•	How different embedding dimensions capture different frequencies
	•	Visualizing positional encodings using heatmaps
	•	Understanding the diagonal wave patterns in the plot

Everything is explained with code + intuition, not just formulas.

⸻

Core Idea (In Simple Words)

Each token position gets a unique vector.

These vectors:
	•	Have the same dimension as token embeddings
	•	Are added to token embeddings
	•	Encode position using smooth sinusoidal waves
	•	Allow the model to infer relative positions
