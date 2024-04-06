
import re

class PasswordChecker:
    def __init__(self, password):
        self.password = password
        self.length = len(password)
        self.uppercase = any(c.isupper() for c in password)
        self.lowercase = any(c.islower() for c in password)
        self.digits = any(c.isdigit() for c in password)
        self.special_chars = re.findall(r'[!@#$%^&*(),.?":{}|<>]', password)

    def check_length(self):
        return self.length >= 8

    def check_uppercase(self):
        return self.uppercase()

    def check_lowercase(self):
        return self.lowercase()

    def check_digits(self):
        return self. digits()

    def check_special_chars(self):
        return bool(self.special_chars)

    def assess_strength(self):
        criteria_checks = [
            self.check_length(),
            self.check_uppercase(),
            self.check_lowercase(),
            self.check_digits(),
            self.check_special_chars()
        ]
        score = sum(criteria_checks)
        if score == 5:
            return "Strong"
        elif score >= 3:
            return "Moderate"
        else:
            return "Weak"

    def feedback(self):
        feedback_msgs = []
        if not self.check_length():
            feedback_msgs.append("Password should be at least 8 characters long.")
        if not self.check_uppercase():
            feedback_msgs.append("Password should contain at least one uppercase letter.")
        if not self.check_lowercase():
            feedback_msgs.append("Password should contain at least one lowercase letter.")
        if not self.check_digits():
            feedback_msgs.append("Password should contain at least one digit.")
        if not self.check_special_chars():
            feedback_msgs.append("Password should contain at least one special character (!@#$%^&*(),.?\":{}|<>).")
        return feedback_msgs


# User Input
password = input("Enter your password: ")
checker = PasswordChecker(password)
strength = checker.assess_strength()
feedback_msgs = checker.feedback()

print(f"Password strength: {strength}")
if feedback_msgs:
    print("Feedback:")
    for msg in feedback_msgs:
        print(f"- {msg}")

