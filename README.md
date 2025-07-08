# Clinical Trial Patient Matching System

This project aims to assist in matching patients with suitable clinical trials based on their medical history and the eligibility criteria defined by various trials. It implements and compares three approaches:

1. **Rule-Based Matching**
2. **Semantic Matching using Sentence-BERT**
3. **Hybrid Matching System** (combines the above two)

This system is designed to support healthcare professionals and researchers in finding relevant trials quickly and accurately.

---

##  Features

- Match patients using strict eligibility rules (age, gender, conditions)
- Match based on semantic understanding of unstructured medical text using BERT
- Combine both logic and language intelligence for best results
- Easily adaptable to different datasets

It implements three approaches:

## 1. Rule-Based Matching

**How it works:**

Uses structured filters such as:

- Age range
- Gender match
- Exclusion keyword check

Matches patients only if they strictly meet these hard-coded rules.

**Pros:**

- Fast and interpretable
- Ensures only eligible patients are matched

**Cons:**

- Doesn't handle complex or free-text descriptions well
- Can miss potential matches due to rigid logic

---

## 2. Semantic Similarity Matching (BERT)

**How it works:**

Uses a pre-trained Sentence-BERT model to convert:

- Patient descriptions
- Trial inclusion/exclusion criteria

into semantic vector embeddings.  
Matches are based on cosine similarity between these vectors.

**Pros:**

- Understands meaning, not just keywords
- Works well on real-world, unstructured text

**Cons:**

- Ignores hard constraints like age/gender
- May suggest incorrect matches without domain filters

---

## 3. Hybrid Matching System

**How it works:**

Combines rule-based filtering and semantic similarity scoring:

- Filters patients based on age, gender, and exclusion criteria
- Then applies BERT-based similarity scoring
- Only eligible patients are semantically matched

**Pros:**

- Best of both worlds: accurate, meaningful, and safe
- Ideal for real-world scenarios involving medical data

**Cons:**

- Slightly more complex and computationally heavier

---

## Technologies Used

- Python (Pandas, NumPy)
- Sentence-BERT via `sentence-transformers`
- Scikit-learn (optional for extensions)
- Jupyter Notebook / Google Colab
- Sample patient and trial datasets (manually generated)
