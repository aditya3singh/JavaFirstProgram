# JavaFirstProgram
//This Java code takes a phrase that the user enters as input and converts it into an acronym. The acronym is created by taking the first letter of each word in the phrase. Here is an explanation of how the code achieves this functionality..


import java.util.Scanner;

public class AcronymGenerator {

    public static String getAcronym(String phrase) {
        // Remove "of" (case-insensitive)
        phrase = phrase.replaceAll("(?i)of", "");

        // Split the phrase into words
        String[] words = phrase.split("\\s+");

        StringBuilder acronym = new StringBuilder();
        for (String word : words) {
            // Get the first character (uppercase)
            acronym.append(Character.toUpperCase(word.charAt(0)));
        }

        return acronym.toString();
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the phrase: ");
        String input1 = scanner.nextLine();
        System.out.println("The acronym is: " + getAcronym(input1));

        System.out.print("Enter the phrase: ");
        String input2 = scanner.nextLine();
        System.out.println("The acronym is: " + getAcronym(input2));

        System.out.print("Enter the phrase: ");
        String input3 = scanner.nextLine();
        System.out.println("The acronym is: " + getAcronym(input3));

        scanner.close();
    }
}
