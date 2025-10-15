# External POST Connectivity Tester

This simple, single-page web application allows you to test external POST request connectivity to any specified URL. It's built with HTML, JavaScript, and styled with Tailwind CSS for a modern, responsive user interface.

## Features

*   **POST Request Testing:** Easily send POST requests to any target URL.
*   **Custom JSON Body:** Provide a custom JSON payload for your POST requests.
*   **Real-time Feedback:** View the HTTP status code, response headers, and response body immediately.
*   **Error Handling:** Displays clear error messages for network issues, invalid JSON, or HTTP errors.
*   **Fully Responsive:** Works seamlessly on various screen sizes, from mobile devices to desktop computers.
*   **Single File Application:** All code is contained within `index.html`, making it easy to deploy or share.
*   **Tailwind CSS:** Modern, utility-first styling for a clean and intuitive user experience.

## How to Use

1.  **Download:** Clone this repository or download the `index.html` file.
2.  **Open in Browser:** Open `index.html` directly in your web browser (e.g., Chrome, Firefox, Edge). No server setup is required.
3.  **Enter Target URL:** In the "Target URL" field, enter the full URL to which you want to send the POST request.
    *   *Example:* `https://httpbin.org/post`
4.  **Enter POST Body (JSON):** In the "POST Body (JSON)" textarea, provide the JSON payload you wish to send.
    *   *Example:*
        ```json
        {
          "name": "Test User",
          "email": "test@example.com",
          "data": {
            "version": 1
          }
        }
        ```
    *   Ensure the JSON is valid. If left empty, an empty POST request (without a body) will be sent, but the `Content-Type: application/json` header will still be included.
5.  **Send Request:** Click the "Send POST Request" button.
6.  **View Response:** The application will display the HTTP status, response headers, and response body in the "Response" section. Any errors will be shown in a clear error message.

## Important Note on CORS

When making requests from a web browser, Cross-Origin Resource Sharing (CORS) policies apply. If the target URL is on a different domain than where `index.html` is hosted (which is usually the case when opening `file:///...`), the browser might block the request if the target server does not send appropriate CORS headers (e.g., `Access-Control-Allow-Origin: *`). You might see a "Network Error" or "CORS Error" in such cases. This is a browser security feature, not a limitation of the application itself. For testing APIs that you control, ensure they are configured to allow CORS requests from your origin.

## Development

This is a self-contained HTML file. No build steps or complex development environment is needed. You can simply modify `index.html` with your favorite text editor.

## License

This project is open-source and available under the MIT License. See the `LICENSE` file for full details.
