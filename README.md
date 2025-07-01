# 🔐 Password Security & Strength Evaluation Report

## Objective
Understand what makes a password strong by testing various passwords using online tools and evaluating them against common attack techniques.

---

##  1–4. Password Strength Test Results

| Password         | Length | Components Used            | Strength         | Crack Time      | Feedback Summary                                |
|------------------|--------|-----------------------------|------------------|------------------|--------------------------------------------------|
| `password`       | 8      | Lowercase only              | ❌ Very Weak     | 0 seconds        | Common dictionary word, easily guessable         |
| `Password123`    | 11     | Upper, lower, numbers       | ❌ Very Weak     | 0 seconds        | Predictable; common structure                    |
| `Pass@123`       | 9      | Upper, lower, number, symbol| ❌ Very Weak     | ~20 seconds      | Dictionary word + sequence                       |
| `FEkiU5Uu@4uKEcc`| 15     | All types + long            | ✅ Very Strong   | 8 trillion years | High entropy; like "Fort Knox"                   |

---

## 5. Best Practices for Strong Passwords

- ✅ Use **12–16+ characters**
- ✅ Mix **uppercase**, **lowercase**, **numbers**, and **symbols**
- ✅ Avoid **dictionary words**, **patterns**, or **keyboard sequences**
- ✅ **Never reuse** passwords across sites
- ✅ Use a **password manager** to generate/store complex passwords

---

## 6. Tips Learned

- 🔸 Password **length is critical** — more characters exponentially increases strength.
- 🔸 "Pass@123" looks strong but is still weak due to predictable structure.
- 🔸 Strong passwords like `FEkiU5Uu@4uKEcc` are **long, random**, and **hard to guess**.

---

## 7. Common Password Attacks

### ✅ Real Example: Hydra Dictionary Attack

Command used:

hydra -l msfadmin -P /root/msfpass.txt ftp://192.168.0.136
 Result:

Username: msfadmin

Password: msfadmin (found in wordlist)

Time to crack: Seconds

 Attack Types
Attack Type	Description
Brute Force	Tries all character combinations (slow on strong passwords)
Dictionary Attack	Uses a wordlist of common passwords
Hybrid Attack	Dictionary + predictable mutations (e.g., Password123)
Credential Stuffing	Tries leaked credentials from other breaches

 8. How Complexity Affects Security
Factor	Impact on Security
Length	Longer passwords take more time to crack
Randomness	Prevents dictionary/pattern-based guessing
Character Variety	Increases entropy, adds protection
Common Phrases	Easily cracked even with added symbols (e.g., Pass@123)
Reused Passwords	Vulnerable to credential stuffing attacks

✅ Conclusion
A secure password is:

✅ Long (15+ characters)

✅ Unpredictable

✅ Contains a mix of character types

❌ Avoids dictionary words and reused passwords

#Example of a Strong Password

G7#hW$uP1xXe!J9q
❌ Avoid These:
Password123, Qwerty@123, admin2024, Welcome@123
##  Notes
Tool used: PasswordMonster

Attack tool: Hydra on Kali Linux

Wordlist: msfpass.txt
