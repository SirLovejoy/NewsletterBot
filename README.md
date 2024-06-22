# NewsletterBot
A bot in Python to handle email newsletters involving several components: managing subscriptions, creating and sending emails, and handling unsubscribes.
# Email Newsletter Bot

This is a simple Python bot for managing email newsletter subscriptions and sending newsletters to subscribers. It uses a file-based approach to store subscriber email addresses and the `smtplib` and `email` libraries to send emails.

## Features

- Add new subscribers.
- Remove existing subscribers.
- Send newsletters to all subscribers.

## Prerequisites

- Python 3.6 or higher
- An email account with SMTP access
- `email-validator` library

## Installation

1. Clone the repository or download the script files.
2. Install the required library using pip:

    ```bash
    pip install email-validator
    ```

## Configuration

1. Open the script file and replace the following placeholders with your actual email details:
    - `your_email@example.com` with your email address
    - `Your Name` with your name
    - `your_password` with your email account password
    - `smtp.example.com` with your SMTP server details (e.g., `smtp.gmail.com` for Gmail)

    ```python
    sender_email = "your_email@example.com"  # Replace with your email
    sender_name = "Your Name"  # Replace with your name
    password = "your_password"  # Replace with your email account password
    ```

## Usage

1. **Add Subscribers:**
   
    Use the `add_subscriber(email)` function to add a new subscriber.
    
    ```python
    add_subscriber("new_subscriber@example.com")
    ```

2. **Remove Subscribers:**
   
    Use the `remove_subscriber(email)` function to remove a subscriber.
    
    ```python
    remove_subscriber("subscriber_to_remove@example.com")
    ```

3. **Send Newsletter:**
   
    Use the `send_newsletter(subject, content)` function to send a newsletter to all subscribers.
    
    ```python
    send_newsletter("Monthly Newsletter", "This is the content of the monthly newsletter.")
    ```

## Example

Here is an example of how to use the bot:

```python
if __name__ == "__main__":
    # Add subscribers
    add_subscriber("test1@example.com")
    add_subscriber("test2@example.com")
    
    # Remove a subscriber
    remove_subscriber("test1@example.com")

    # Send a newsletter
    send_newsletter("Monthly Newsletter", "This is the content of the monthly newsletter.")
