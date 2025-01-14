
# masa-exam

## Part I: Theory

*Please, do NOT use online resources as an assistance for this part of the exam*


## Section A: Please, select the correct answer or the most close to the correct one *=> 20 points:*

1. **What is a PR?** *=> 2 points*
 - [ ] Program Result: the outcome of a programming effort available for testing
 - [ ] Public Relations: a practice of managing and influencing an organizational info to the public
 - [x] Pull Request: a request to review the code of a developer prior to merging it main branch
 - [ ] Private Role: A security role that is used in internal system processing

2. **What is the role of a service in nodejs server architecture?** *=> 2 points*
 - [x] Get the request from the router, treat the request parameters, prepare the response of the server to the consumer
 - [ ] Keep state of a specific logic portion of the system, provide processing of the data passed from the different controllers, parse the data and returned the processed response
 - [ ] To be the first element in the system that should service the consumer for his CRUD request to the server
 - [ ] To provide services to the system that do not require a state but should be used across the whole system

3. **What is INNER JOIN?** *=> 2 points*
 - [ ] A mechanism to link between to tables in the SQL query to bring data based on the same value in two tables. Allows NULL values on one on the sides of the JOIN
 - [x] A mechanism to link between to tables in the SQL query to bring data based on the same value in two tables. Only non NULL values are accepted for both sides of the JOIN
 - [ ] A way of executing to `foreach` loops in JS/TS while the internal loop uses values of the external loop
 - [ ] Such a term does not exist

4. **What is the code of a server error in HTTP protocol?** *=> 2 points*
 - [ ] 2xx
 - [ ] 3xx
 - [ ] 4xx
 - [x] 5xx


5. **What is the correct flow a story?** *=> 2 points*
 - [ ] Software Detailed Design (SDD), Product design, QA review, UI design, Development, QA testing, Customer review
 - [x] Customer request, Product design, UI design, SDD, QA review, Development, QA testing, Customer User Acceptance Testing (UAT)
 - [ ] Product design, SDD, QA review, UI design, Development, QA testing, UAT
 - [ ] Customer request, UI design, Product design, UAT, QA review, Development, QA testing

6. **Which tool would you use to test a nodejs server?** *=> 2 points*
 - [ ] Browser
 - [ ] Postman
 - [ ] Fiddler
 - [x] All answers are correct

7. **What is the most secure way to connect to SQL Server?** *=> 2 points*
 - [ ] Integrated security
 - [x] Mixed mode
 - [ ] SQL Server login
 - [ ] Application role

8. **What is the correct pair of a protocol and the port for secure HTTP communication?** *=> 2 points*
 - [ ] HTTP:80
 - [ ] HTTPS:80
 - [x] HTTPS:443
 - [ ] HTTP:443

9. **What is a trigger?** *=> 2 points*
 - [x] Trigger is a piece of code executed by the database engine whenever some action is performed on a database object like tables, view, etc.
 - [ ] Trigger is a method that is called JS/TS environment whenever a certain event is fired to complete an asynchronous code execution
 - [ ] Trigger is a processing being performed right after the merge of a code to main branch in order to run a build for the system
 - [ ] Trigger is the mechanism by which the router is sending its data to the controller in nodejs server

10. **Why would you use the JWT token? (more than a single answer can be selected)** *=> 2 points*
 - [x] JWT tokens are encrypted
 - [ ] It's a more secure way of handling authentication and authorization data than username and password
 - [x] JWT tokens are signed and this signature can be verified uniquely
 - [ ] All answers are correct


## Section B: Please, explain the following terms the best way you can *=> 22 points*

11. **Authentication & Authorization** *=> 7 points*
	Authentication is a process of entering a system using username and password.
	The system compares a username and password that were entered and compares it 
	to the username/password which is stored in a DB. After user has passed authentication, 
	authorization comes into play. Authorization defines which level of acces this user has.
12. **Stored procedure** *=> 3 points*
Stored procedure is a set of SQL instructions which are executed once and then stores in a DB.
It helps to save time and resources when doing frequent requests and increases performance also.
13. **Git rebase** *=> 4 points*
Git rebase rearranges commits one by one from an alternative branch to the top of the main branch 
14. **Generics** *=> 4 points*
Generics are reusable components which could be used with a different types. 
15. **Middleware** *=> 4 points*
Middleware is a software which connects different comoponents and services
 
## Part II: Practice on paper *=> 45 points*

*No restrictions on online resources usage. You also may use your development machine for assistance in debugging if needed.*

16. **You received a bug stating the following: "Intermittently the following method results in a system getting stuck." You're required to find and fix the problem in this method:** *=> 10 points*

function addMonths(date: Date, value: number): Date 
{
    let expectedMonth: number = date.getMonth() + value;
  if (expectedMonth > 11) 
        expectedMonth = expectedMonth % 12;

    date.setMonth(expectedMonth);
  if (date.getMonth() > expectedMonth) date.setDate(0);    
    return date;
}

17. **Having the following DB tables diagram:** *=> 10 points*

![](https://github.com/lentyaishe/masa-exam/blob/dev/resources/db-relations.jpg)

You need to write a query that returns for each student his/her parents' information/ Take into consideration that the amount of parents for the child can be different ("Orphan" comment should appear for any child that has no parents defined in the tables). The data should be returned in the following manner:

| Student | Parents |
| --- | --- |
| John Doe | Mark Doe (09-1231231), Jane Doe (09-4132123) |
| Mary Smith | Klark Smith (07-2134897) |
| Patrice Raymond | Orphan |

18. **Write a method in JS/TS that gets as an argument an array of numbers and returns the sum of all array members**. *=> 5 points*

	function sumArray(arr){
		var sum = 0;
		for (int i = 0; i < arr.length; i++){
			sum = sum + arr.i;
		}
		return sum;
	}

19. **Explain the following piece of code:** *=> 5 points*

		public static padLeft(input: number, places: number): string {
			const zeroes: number = places - input.toString().length + 1;
			return Array(+(zeroes > 0 && zeroes)).join("0") + input.toString();
		}

		This function gets two numbers: number1 and number2 and returns a number1 with number2 digits in it. If number1 < number2 it adds (number2 - number1) zeros to the end. 
		If number1 = number 2 it returns number1. If number1 > number2 it returns first number2 digits in number1.

20. **Fix the following code and fill the required gaps in it by the coding standards. The purpose of this code is to verify the user is a member of a specific role and in case the user is the user data is returned by the isUserPermitted() method. Treat the comments as actual code written that should not be changed:** *=> 15 points*

		interface user {
			id: number;
			firstName: string;
			lastName: string;
		}
		
		interface dbUser {
			id: number;
			first_name: string;
			last_name: string;
		}
		
		interface role {
			id: number;
			userIds: number[];
		}
		
		interface dbRole {
			id: number;
			user_id: number;
		}
		
		public isUserPermitted(userId: number, roleId: number): Promise<user> {
			return new Promise<user>((resolve, reject) => {
				Promise.all([
					this.getUser(userId),
					this.getRole(roleId)
				])
				.then((results: [user | role]) => {
					return results[1].userIds.indexOf(results[0].id) > -1;
					resolve(results[0]);
				});
			});
		}
		
		private getUser(userId: number): Promise<user> {
			return new Promise<user>((resolve, reject) => {
				// Access to the DB that returns the user data by id as dbUser or null
			});
		}
		
		private getRole(roleId: number): Promise<role> {
			return new Promise<user>((resolve, reject) => {
				// Access to the DB that returns the role data by id as array of dbRole or null
			});
		}


## Part III: Practice on dev machine *=> 33 points*

*No restrictions on online resources usage*

 - Clone the repository: https://github.com/lentyaishe/masa-exam;
 - Switch to `broken-server` branch;
 - Create a new git repository under your personal Github called `masa-exam`;
 - Load the `main` branch of your new repository with the contents of the `broken-server` branch;
 - Each bug in the list should be solved in designated branch.

The following is the list of currently existing problems with the system. :

21. **The server solution cannot be compiled. Fix all compilation issues accordingly.** *=> 10 points*

22. **An attempt to get a list of board types fails.** *=> 5 points*

23. **Any request to the server returns: "A token is required for authentication" even in case the token is supplied for the request.** *=> 5 points*

24. **Addition of the new user cannot be performed. Returned error message: "Incorrect query".** *=> 5 points*

25. **On an attempt to add a new board type an error: "not found" is returned.** *=> 8 points*

# Good luck!!
