#include <stdio.h>
#include <string.h>

enum designation {
    accountant,
    clerk
};

struct employee {
    int employeeid;
    char employeename[50];
    enum designation emp_designation;
    float employeesalary;
    char dateofjoining[11];
    int yearsofexperience;
};

float calculateAccountantBonus(float employeesalary, int yearsofexperience) 
{
    if (yearsofexperience > 5) 
    {
        return 0.10 * employeesalary;
    } else if (yearsofexperience >= 3) 
    {
        return 0.05 * employeesalary;
    } else 
    {
        return 0.02 * employeesalary;
    }
}

float calculateClerkBonus(float employeesalary, int yearsofexperience) 
{
    if (yearsofexperience > 5) 
    {
        return 0.15 * employeesalary;
    } 
    else if (yearsofexperience >= 3) 
    {
        return 0.10 * employeesalary;
    } else 
    
    {
        return 0.05 * employeesalary;
    }
}

int main() {
    struct employee e[10];
    int i;
    for (i = 0; i < 10; i++) 
    {
        printf("Enter the employee ID:");
        scanf("%d", &e[i].employeeid);
        
        printf("Enter the employee name:");
        scanf("%s", e[i].employeename);
        
        printf("Enter the employee salary:");
        scanf("%f", &e[i].employeesalary);
        
        printf("Enter the date of joining (YYYY-MM-DD):");
        scanf("%s", e[i].dateofjoining);
        
        printf("Enter the employee experience:");
        scanf("%d", &e[i].yearsofexperience);
        
        printf("Enter the employee designation (0 for accountant, 1 for clerk):");
        int desig;
        scanf("%d", &desig);
        e[i].emp_designation = (enum designation)desig;

        float bonus;
        if (e[i].emp_designation == accountant) 
        {
            bonus = calculateAccountantBonus(e[i].employeesalary, e[i].yearsofexperience);
        }
        else 
        {
            bonus = calculateClerkBonus(e[i].employeesalary, e[i].yearsofexperience);
        }

        printf("Employee ID: %d, Name: %s, Salary: %.2f, Date of Joining: %s, Experience: %d years, Designation: %s, Bonus: %.2f\n",
               e[i].employeeid, e[i].employeename, e[i].employeesalary, e[i].dateofjoining, e[i].yearsofexperience,
               e[i].emp_designation == accountant ? "Accountant" : "Clerk", bonus);
    }

    return 0;
}
