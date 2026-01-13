Hi,
The task took 3:52 hours to complete.

1. How to run the application

Requirements:
- .NET Framework 4.0
- Visual Studio

Steps:
1) Download and extract the provided ZIP archive.
2) Open the solution file (Test.sln) in Visual Studio.
3) Restore NuGet packages if Visual Studio asks for it.
4) Build the solution and run the application.

After запускa the application will open in a small desktop window.

2. Why I chose WinForms instead of WPF

I chose WinForms because I have more practical experience with it.
Using WinForms allowed me to focus on the core functionality of the task, API integration, and error handling within the given time frame.

I have not worked with WPF before, and for this test task I preferred to use a framework I am more comfortable with to deliver a stable and working solution.

3. How API errors are handled

All API calls are performed asynchronously using HttpClient.

HTTP responses are checked before processing the data. If a request fails due to network issues or an unsuccessful HTTP status code, an exception is raised and handled in the UI layer.

The API response itself is also checked for API-level errors. If the API returns an error message, it is shown to the user in the application interface.

All errors are displayed directly in the UI, and the application remains responsive.

4. What I would improve with more time

With more time, I would verify the actual conversion logic using a fully available currency conversion API to ensure that real exchange rates are returned correctly.

I would also extend the list of supported currencies and add more options (at least 5–10) to the dropdown lists.

Another improvement would be adding reverse conversion, where the user could enter a value in the result field and convert it back to the original currency.

5. Security considerations when working with APIs

In a real-world application, API keys or access tokens should never be hardcoded or committed to a repository. They should be stored securely, for example using environment variables or external configuration files.

All API requests should be made over HTTPS to protect transmitted data.

It is also important to handle errors carefully so that internal details are not exposed to the user. Input validation and request limiting should be considered to prevent abuse or incorrect usage of the API.
