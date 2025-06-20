# Chapter 18: Reinforcement Learning (RL)

## 1. Definisi
Reinforcement Learning adalah pembelajaran berbasis interaksi:
- **Agen**: pengambil keputusan
- **Lingkungan**: tempat agen beroperasi
- **Reward**: sinyal kinerja
- **Policy**: strategi agen
- **State**: representasi kondisi saat ini
- **Action**: pilihan agen

## 2. Goal RL
Menemukan **policy** yang memaksimalkan total expected reward jangka panjang.

## 3. Algoritma RL Umum
### a. Policy Gradient
- Melatih model langsung untuk memaksimalkan reward
- Menggunakan optimisasi gradien untuk memperbarui parameter policy

### b. Q-Learning
- Mengestimasi fungsi Q(s, a): seberapa bagus memilih action a pada state s
- Gunakan update:
\[
Q(s, a) \leftarrow Q(s, a) + \alpha [r + \gamma \max_a' Q(s', a') - Q(s, a)]
\]

## 4. Teknik RL Lainnya
- **Actor-Critic**: gabungan policy gradient dan Q-learning
- **Deep Q-Networks (DQN)**: gunakan NN untuk mendekati Q
- **Exploration vs Exploitation**: keseimbangan antara mencoba hal baru vs menggunakan yang terbaik

## 5. Tools
- **OpenAI Gym**: lingkungan RL standar
- **TF-Agents**: framework RL dari TensorFlow
- **Stable Baselines**: library RL populer berbasis PyTorch

## 6. Tantangan RL
- Sparse reward (reward jarang muncul)
- High variance dalam hasil training
- Sulit diskalakan ke dunia nyata
