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
    string[] questions = new string[] { };
    string[][] options = new string[][] { };
    string[] answers = new string[] { };

    if (selectedOption == 1)
    {
        questions = new string[]
 {
    "What is the capital of Australia?",
    "Who painted the Mona Lisa?",
    "In which country is the Great Wall located?",
    "What is the largest planet in our solar system?",
    "Who wrote the play 'Romeo and Juliet'?",
    "Which ocean is the largest by area?",
    "What is the chemical symbol for gold?",
    "Which city is known as the 'Big Apple'?",
    "Which is the tallest mountain in the world?",
    "What is the largest organ in the human body?"
 };


        options = new string[][]
       {
    new string[] { "A) Canberra", "B) Sydney", "C) Melbourne", "D) Perth" },
    new string[] { "A) Vincent van Gogh", "B) Pablo Picasso", "C) Leonardo da Vinci", "D) Michelangelo" },
    new string[] { "A) China", "B) Japan", "C) India", "D) Australia" },
    new string[] { "A) Jupiter", "B) Saturn", "C) Earth", "D) Mars" },
    new string[] { "A) William Shakespeare", "B) Jane Austen", "C) Charles Dickens", "D) Mark Twain" },
    new string[] { "A) Pacific Ocean", "B) Atlantic Ocean", "C) Indian Ocean", "D) Arctic Ocean" },
    new string[] { "A) Au", "B) Ag", "C) Fe", "D) Hg" },
    new string[] { "A) New York City", "B) Los Angeles", "C) Chicago", "D) Miami" },
    new string[] { "A) Mount Everest", "B) K2", "C) Mount Kilimanjaro", "D) Mauna Kea" },
    new string[] { "A) Skin", "B) Liver", "C) Heart", "D) Brain" }
       };



        answers = new string[]
       {
    "A",
    "C",
    "A",
    "B",
    "A",
    "A",
    "A",
    "A",
    "A",
    "A"
       };

    }
    else if (selectedOption == 2) {
        questions = new string[] {
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
        options = new string[][]
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
        answers = new string[] { "A", "A", "A", "C", "C", "A", "B", "A", "C", "A" };
    }
    else if (selectedOption == 3)
    {
        questions = new string[]
  {
    "What is C#?",
    "What is an interface in C#?",
    "What is the difference between classes and structs in C#?",
    "What is the purpose of 'using' directive in C#?",
    "What is the default access modifier for a class member in C#?",
    "What is the difference between 'readonly' and 'const' in C#?",
    "What is a delegate in C#?",
    "What is the purpose of the 'async' and 'await' keywords in C#?",
    "What is a generic class in C#?",
    "What is the difference between 'throw' and 'throw ex' in C#?"
  };
        options = new string[][]
{
    new string[] { "A) A programming language", "B) A software framework", "C) A type of variable", "D) None of the above" },
    new string[] { "A) A class that can be instantiated", "B) A collection of method declarations", "C) A blueprint for a class", "D) None of the above" },
    new string[] { "A) Classes are reference types, and structs are value types", "B) Classes can be inherited, and structs cannot", "C) Structs are stored on the stack, and classes are stored on the heap", "D) None of the above" },
    new string[] { "A) To import namespaces", "B) To define variables", "C) To handle exceptions", "D) None of the above" },
    new string[] { "A) Public", "B) Protected", "C) Private", "D) Internal" },
    new string[] { "A) 'readonly' variables can be assigned a value only at runtime", "B) 'const' variables can be changed during runtime", "C) 'readonly' variables are initialized at compile-time", "D) 'const' variables can be modified after initialization" },
    new string[] { "A) A reference to a method", "B) A container for storing objects", "C) A base class for all classes", "D) None of the above" },
    new string[] { "A) 'async' is used to define asynchronous methods, and 'await' is used to await the completion of an asynchronous operation", "B) 'async' and 'await' are used to define synchronous methods", "C) 'async' is used to define synchronous methods, and 'await' is used to await the completion of a synchronous operation", "D) 'async' and 'await' are used to define parallel execution" },
    new string[] { "A) A class that can only accept a specific type of data", "B) A class that can be accessed from any other class", "C) A class that can be reused for different types", "D) None of the above" },
    new string[] { "A) 'throw' preserves the original stack trace, and 'throw ex' replaces it with the current stack trace", "B) 'throw ex' preserves the original stack trace, and 'throw' replaces it with the current stack trace", "C) 'throw' rethrows the exception, and 'throw ex' throws a new exception", "D) 'throw' and 'throw ex' are equivalent in functionality" }
};
        answers = new string[]
{
    "A",
    "C",
    "A",
    "A",
    "C",
    "C",
    "A",
    "A",
    "C",
    "A"
};
    }
    else
    {

        Console.WriteLine("Invalid Chooice");

    }

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

        if (choicetheoption.ToUpper() == "A" || choicetheoption.ToUpper() == "B" || choicetheoption.ToUpper() == "C"|| choicetheoption.ToUpper() == "D")
        {

           
            if (choicetheoption.ToUpper() == answers[i])
            {
                score++;
            }
        }
        else
            Console.WriteLine("Incorrect Answer");
    };

    Console.WriteLine("You have scored {0} out of {1}",score,questions.Length);
}
else
{
    Console.WriteLine("Invalid choice.");
}



