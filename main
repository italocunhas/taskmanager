import java.util.ArrayList;
import java.util.Scanner;

class Task {
    private String description;
    private boolean isCompleted;

    public Task(String description) {
        this.description = description;
        this.isCompleted = false;
    }

    public void markAsCompleted() {
        this.isCompleted = true;
    }

    @Override
    public String toString() {
        return (isCompleted ? "[X] " : "[ ] ") + description;
    }
}

public class TaskManager {
    private static ArrayList<Task> tasks = new ArrayList<>();

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String command;

        do {
            System.out.println("\nTask Manager:");
            System.out.println("1. Add Task");
            System.out.println("2. Remove Task");
            System.out.println("3. List Tasks");
            System.out.println("4. Mark Task as Completed");
            System.out.println("0. Exit");
            System.out.print("Enter command: ");
            command = scanner.nextLine();

            switch (command) {
                case "1":
                    System.out.print("Enter task description: ");
                    String description = scanner.nextLine();
                    tasks.add(new Task(description));
                    break;

                case "2":
                    System.out.println("Tasks:");
                    for (int i = 0; i < tasks.size(); i++) {
                        System.out.println(i + ". " + tasks.get(i));
                    }
                    System.out.print("Enter task number to remove: ");
                    int indexToRemove = Integer.parseInt(scanner.nextLine());
                    if (indexToRemove >= 0 && indexToRemove < tasks.size()) {
                        tasks.remove(indexToRemove);
                    } else {
                        System.out.println("Invalid task number.");
                    }
                    break;

                case "3":
                    System.out.println("Tasks:");
                    for (int i = 0; i < tasks.size(); i++) {
                        System.out.println(i + ". " + tasks.get(i));
                    }
                    break;

                case "4":
                    System.out.println("Tasks:");
                    for (int i = 0; i < tasks.size(); i++) {
                        System.out.println(i + ". " + tasks.get(i));
                    }
                    System.out.print("Enter task number to mark as completed: ");
                    int indexToComplete = Integer.parseInt(scanner.nextLine());
                    if (indexToComplete >= 0 && indexToComplete < tasks.size()) {
                        tasks.get(indexToComplete).markAsCompleted();
                    } else {
                        System.out.println("Invalid task number.");
                    }
                    break;

                case "0":
                    System.out.println("Exiting...");
                    break;

                default:
                    System.out.println("Invalid command.");
            }
        } while (!command.equals("0"));

        scanner.close();
    }
}
