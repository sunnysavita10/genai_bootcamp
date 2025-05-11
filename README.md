```
conda create -p venv python=3.10 -y
```

```
pip install -r requirements.txt
```

```
pip install ipykernel
```
```
git filter-repo --force --path final_transformer_translation_model.pt --invert-paths
```

| 🔢 Step | 🛠️ Command                                                                    | 📋 Purpose                                                        |
| ------- | ------------------------------------------------------------------------------ | ----------------------------------------------------------------- |
| 1       | `git clone https://github.com/sunnysavita10/genai_bootcamp.git cleaned_repo`   | Fresh clone banata hai jahan destructive operations safe hain     |
| 2       | `cd cleaned_repo`                                                              | Cloned repo ke andar jaate hain                                   |
| 3       | `git filter-repo --path final_transformer_translation_model.pt --invert-paths` | Pure Git history se `.pt` file delete karta hai                   |
| 4       | `echo "*.pt" >> .gitignore`                                                    | `.pt` files ko ignore karne ke liye `.gitignore` me add karta hai |
| 5       | `git add .gitignore`                                                           | `.gitignore` file ko Git staging me daalta hai                    |
| 6       | `git commit -m "Ignore .pt files"`                                             | Ignore changes ko commit karta hai                                |
| 7       | `git push origin --force`                                                      | Cleaned repo ko GitHub par forcefully push karta hai              |


| 🔢 Step | 🛠️ Command                                                                            | 📋 Purpose                                                     |
| ------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------- |
| Alt 1   | `git filter-repo --force --path final_transformer_translation_model.pt --invert-paths` | Existing repo me forcefully file delete karta hai (⚠️ riskier) |
