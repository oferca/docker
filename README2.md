No worries! If you already initialized the submodule, you just need to **switch it to the branch you want** and update it. Here’s how:

---

### 1️⃣ Go into the submodule

```bash
cd calcom
```

---

### 2️⃣ Fetch all branches from your fork

```bash
git fetch origin
```

---

### 3️⃣ Checkout the branch `v5.3.3`

```bash
git checkout v5.3.3
```

---

### 4️⃣ Pull the latest changes on that branch

```bash
git pull origin v5.3.3
```

---

### 5️⃣ Go back to the parent repo and record the submodule state

```bash
cd ..
git add calcom
git commit -m "Update calcom submodule to branch v5.3.3"
```

---

💡 **Tip:** After this, you can make the submodule **always track that branch** by updating `.gitmodules`:

```ini
[submodule "calcom"]
    path = calcom
    url = https://github.com/oferk1/cal.com.git
    branch = v5.3.3
```

Then in the future, you can run:

```bash
git submodule update --remote --merge
```

…and it will pull the latest from `v5.3.3` automatically.

---

If you want, I can give a **full sequence of commands** to go from a fresh clone to a submodule on `v5.3.3` in one go. This avoids doing things manually each time. Do you want me to do that?
