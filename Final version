"""This is my integration project that will take the input that the user enters
and give back the amount of calories they are required to gain or lose in order
to reach their goal of gaining, losing or maintaining weight"""
__author__ = "Mijail Hurtado"


# Integration Project
# COP 1500
# Professor Vanselow


def get_bmr():
    """The purpose of this function is to determine the user's
    basal metabolic rate (bmr) by asking a few questions and
    plugging them into a formula. Once the bmr is determined it is returned
    back to the main function"""
    gender = input("What is your gender: M or F?")
    age = int(input("What is your age?"))
    height = int(input("What is your height in inches?"))
    weight = (int(input("What is your weight in pounds?")))
    bmr_wght_constant = 4.536
    bmr_hght_constant = 15.88
    bmr_age_constant = 5
    if gender == 'M':
        bmr = int((bmr_wght_constant * weight) + (bmr_hght_constant * height) - (bmr_age_constant * age) + 5)
    elif gender == 'F':
        bmr = int((bmr_wght_constant * weight) + (bmr_hght_constant * height) - (bmr_age_constant * age) - 161)
    else:
        print("Please try again.")
    return bmr


def get_daily_calorie_requirement(bmr):
    """After the bmr has been determined this function uses
    the result and asks the fitness level of the user in order
    to determine the daily caloric intake of the user. Once the
    daily amount of calories required is determined it is returned to the
    main function"""
    dcr_1 = 1.2
    dcr_2 = 1.375
    dcr_3 = 1.55
    dcr_4 = 1.725
    dcr_5 = 1.9
    act_lvl = int(input("What is your activity level?"))
    if act_lvl == 1:
        daily_calorie_requirement = int(bmr * dcr_1)
    elif act_lvl == 2:
        daily_calorie_requirement = int(bmr * dcr_2)
    elif act_lvl == 3:
        daily_calorie_requirement = int(bmr * dcr_3)
    elif act_lvl == 4:
        daily_calorie_requirement = int(bmr * dcr_4)
    elif act_lvl == 5:
        daily_calorie_requirement = int(bmr * dcr_5)
    else:
        print("Please choose a number 1-5.")
    return daily_calorie_requirement


def main():
    """This is the main function that tells the user what is the purpose
    of the program and calls on the functions get_daily_calorie_requirement and get_bmr
    to get information necessary to get the program moving along. It take the daily_calorie_requirement
    and matches it up with the users goal allowing them to see
    how many calories they have consumed for the day and when
    they reach the amount of calories for them to reach their goals"""
    print("Hello, welcome to my integration project!")
    print("The purpose of this program is to help the user reach their goal and provide helpful suggestions.")
    print("It will do this by taking your age, gender, height and your level of physical activity in order to"
          "calculate your Basal Metabolic Rate(BMR)")
    print("Your BMR is how many calories you burn in a single day. Combining your BMR with your goals we can suggest a"
          "meal plan and exercises that will help reach your goals")
    print("Let's get started! I will start by asking you a few questions in order to make a profile and give you the"
          "best informed advice.")
    bmr = get_bmr()
    print("Your BMR is: ", bmr)

    print("Great! Now that we have calculated your Basal Metabolic Rate, let's calculate your daily calorie"
          "requirement!")
    print("This is the calories you should be taking in to maintain your current weight")
    print("How active are you on a scale of 1-5?")
    print("1 being  you are sedentary (little to no exercise)")
    print("2 being lightly active (light exercise or sports 1-3 days a week)")
    print("3 being moderately active (moderate exercise 3-5 days a week)")
    print("4 being very active (hard exercise 6-7 days a week)")
    print("5 being super active (very hard exercise and a physical job)")
    print("Exercise would be 15 to 30 minutes of having an elevated heart rate.")
    print("Hard exercise would be 2 plus hours of elevated heart rate.")
    daily_calorie_requirement = get_daily_calorie_requirement(bmr)
    print("The amount of calories you should be consuming are: ", daily_calorie_requirement)
    print("Now that we have calculated your daily caloric requirement, let's figure out your goals.")
    print("If you are trying to lose weight enter 1, if you are trying to maintain enter 2 or if you are trying to"
          "gain weight enter 3.")
    goal = int(input("What is the goal you are setting for yourself?"))
    if goal == 1:
        print("In order to reach your goal safely you will have to reduce your daily caloric intake by 500 in order to"
              "lose one pound a week")
        print("In order to reach your goal, will keep track of the amount of calories you consume.")
        print("The best way to keep track of your calories is to record the amount of calories consumed after"
              "every meal.")
        cal_goal_1 = daily_calorie_requirement - 500
        cal_consumed_1 = 0
        while cal_goal_1 >= cal_consumed_1:
            cal_taken = int(input("How many calories have was your last meal?"))
            cal_consumed_1 += cal_taken
        if cal_goal_1 <= cal_consumed_1:
            print("Congratulations! You have reached your goal for the day by taking in", cal_consumed_1, "calories!")

    elif goal == 2:
        print("If you are trying to maintain your current level then just continue taking in the same about of calories"
              "daily.")
        print("In order to reach your goal, will keep track of the amount of calories you consume.")
        print("The best way to keep track of your calories is to record the amount of calories consumed after"
              "every meal.")
        cal_goal_2 = daily_calorie_requirement
        cal_consumed_2 = 0
        while cal_goal_2 >= cal_consumed_2:
            cal_taken = int(input("How many calories have was your last meal?"))
            cal_consumed_2 += cal_taken
        if cal_goal_2 <= cal_consumed_2:
            print("Congratulations! You have reached your goal for the day", cal_consumed_2, "calories!")
    elif goal == 3:
        print("If you want to bulk up and build lean muscle mass you need to consume 300 to 500 more calories than"
              "your daily metabolic requirement")
        print("If you are just starting out, I would suggest you begin with 300 calories as taking more calories than"
              "need will lead to fat also being produced.")
        print("In order to reach your goal safely you will have to increase your daily caloric intake by 300 in order"
              "to gain one half a pound to half a pound a week")
        print("In order to reach your goal, will keep track of the amount of calories you consume.")
        print("The best way to keep track of your calories is to record the amount of calories consumed after"
              "every meal.")
        cal_goal_3 = daily_calorie_requirement + 300
        cal_consumed_3 = 0
        while cal_goal_3 >= cal_consumed_3:
            cal_taken = int(input("How many calories have was your last meal?"))
            cal_consumed_3 += cal_taken
        if cal_goal_3 <= cal_consumed_3:
            print("Congratulations! You have reached your goal for the day!", cal_consumed_3, "calories!")
    else:
        print("Please try again.")


main()
