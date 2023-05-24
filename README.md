# pf-quiz

using System.ComponentModel.Design;

Console.WriteLine("=============================");
Console.WriteLine("Welcome to Quiz Application!!");
Console.WriteLine("=============================");

Console.ReadLine();
Console.WriteLine("Select your level (1-3)");

Console.WriteLine("1:Beginner");
Console.WriteLine("2:Intermediate");
Console.WriteLine("3:Advance");

int selectedOption;

selectedOption = Convert.ToInt32(Console.ReadLine());


if (selectedOption == 1 || selectedOption == 2 || selectedOption == 3)
{

    string[] questions = new string[]
        {
            "What is the capital of France?",
            "Which planet is known as the Red Planet?",
            "What is the chemical symbol for gold?",
            "Who painted the Mona Lisa?",
            "Which country won the FIFA World Cup in 2018?",
            "What is the largest ocean in the world?",
            "Which element has the atomic number 6?",
            "Who wrote the play 'Romeo and Juliet'?",
            "Which city is known as the 'Big Apple'?",
            "What is the tallest mountain in the world?"
        };

    string[][] options = new string[][]
        {
            new string[] { "A. Paris", "B. London", "C. Madrid", "D. Rome" },
            new string[] { "A. Mars", "B. Venus", "C. Jupiter", "D. Saturn" },
            new string[] { "A. Au", "B. Ag", "C. Fe", "D. Hg" },
            new string[] { "A. Vincent van Gogh", "B. Pablo Picasso", "C. Leonardo da Vinci", "D. Michelangelo" },
            new string[] { "A. France", "B. Germany", "C. Brazil", "D. Croatia" },
            new string[] { "A. Pacific Ocean", "B. Atlantic Ocean", "C. Indian Ocean", "D. Arctic Ocean" },
            new string[] { "A. Hydrogen", "B. Carbon", "C. Oxygen", "D. Sodium" },
            new string[] { "A. William Shakespeare", "B. Jane Austen", "C. Charles Dickens", "D. Mark Twain" },
            new string[] { "A. Los Angeles", "B. Chicago", "C. New York City", "D. Miami" },
            new string[] { "A. Mount Everest", "B. K2", "C. Mount Kilimanjaro", "D. Mauna Kea" }
        };

    string[] correctAnswers = new string[] { "A", "A", "A", "C", "C", "A", "B", "A", "C", "A" };

    int score = 0;

    for (int i = 0; i < questions.Length; i++)
    {

        Console.WriteLine("{0}) {1}", i + 1, questions[i]);
        for (int j = 0; j < options[i].Length; j++)
        {
            Console.WriteLine(options[i][j]);

        };
        string choicetheoption;

        choicetheoption = Console.ReadLine();

        Console.WriteLine(choicetheoption  );

        if (choicetheoption.ToUpper() == "A" || choicetheoption.ToUpper() == "B" || choicetheoption.ToUpper() == "C")
        {

           
            if (choicetheoption.ToUpper() == correctAnswers[i])
            {
                score++;
            }
        }
        else
            Console.WriteLine("Incorrect Answer");
    };

    Console.WriteLine("You have scored {0}",score);
}
else
{
    Console.WriteLine("Invalid choice.");
}



