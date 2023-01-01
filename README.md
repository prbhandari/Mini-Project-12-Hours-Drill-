# Mini-Project-12-Hours-Drill-
Quiz Maker 
print("*************************************welcome to the quiz*****************************************")
print("^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^Lets check your skill in python^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^")

from Pyquiz import quiz  

print('lets start:  *******')
score=0
def check_ans(question, ans, attempts, score):
    if quiz[question]['answer'].lower() == ans.lower():
        print(f"Correct Answer! \nYour score is {score + 1}!")
        return True
    else:
        print(f"Wrong Answer :( \nYou have {attempts - 1} left! \nTry again...")
        return False
for question in quiz:
    attempts = 3
    while attempts > 0: 
            print(quiz[question]['question']) 
            answer = input("Enter Answer: ")
            check = check_ans(question, answer, attempts, score)
            if check:
                score += 1
                break
            attempts -= 1
print('hurrayyy......!!!!!!!!!!!!!!!!!! done with the quiz')
