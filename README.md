<div align="center">
  <img height="260" width="260" src="https://github.com/louiseyousre200/hesshub-api/assets/79291748/f5d7e45e-c4fa-482c-9dbc-97d0c235bd8f"/>
</div>

<br/>
<br/>

# HessHub Social Platform API Documentation 📚

Welcome to the Hesses Social Platform API documentation! This API allows you to interact with various features of the social platform, including user management, hesses, likes, followers, privacy preferences, and more.

## Table of Contents 📑

- [Authentication](#authentication-🔐) 🔐
- [Users](#users-👥) 👥
- [User Profile Images](#user-profile-images-🖼️) 🖼️
- [Following](#following-👂) 👂
- [Blocking](#blocking-🚫) 🚫
- [Follow Requests](#follow-requests-🤝) 🤝
- [Hesses](#hesses-🗨️🐍) 🗨️🐍
- [Hess Media Upload and Retrieval](#hess-media-upload-and-retrieval-📷) 📷
- [Likes](#likes-❤️) ❤️
- [Feed](#feed-📰) 📰
- [Search](#search-🔍) 🔍
- [Privacy Preferences](#privacy-preferences-🔒) 🔒
- [Getting Started](#getting-started-🚀) 🚀
- [Contributing](#contributing-🤝) 🤝
- [License](#license-📄) 📄

## Authentication 🔐

- **POST** `/api/auth/login`: User login.
- **POST** `/api/auth/register`: User registration.
- **POST** `/api/auth/forgot-password`: Request a password reset email.
- **POST** `/api/auth/reset-password`: Reset password using a token.
- **POST** `/api/auth/confirm-email`: Confirm user's email using a token.

## Users 👥

- **GET** `/api/users/:id`: Get user details by ID.
- **PUT** `/api/users/:id`: Update user details by ID.
- **DELETE** `/api/users/:id`: Delete a user by ID.

## User Profile Images 🖼️

- **GET** `/api/users/:id/profile-image`: Get user's profile image.
- **PUT** `/api/users/:id/profile-image`: Update user's profile image.
- **DELETE** `/api/users/:id/profile-image`: Delete user's profile image.

## Following 👂

- **POST** `/api/users/:id/follow`: Request to follow a user.
- **PUT** `/api/users/:id/follow`: Update following preferences for a followed user.
- **DELETE** `/api/users/:id/follow`: Unfollow a user.

## Blocking 🚫

- **POST** `/api/users/:id/block`: Block a user.
- **DELETE** `/api/users/:id/block`: Unblock a user.

## Follow Requests 🤝

- **DELETE** `/api/follow-requests/:id`: Cancel a sent follow request.
- **PUT** `/api/follow-requests/:id/approve`: Approve a follow request.
- **PUT** `/api/follow-requests/:id/reject`: Reject a follow request.

## Hesses 🗨️🐍

- **POST** `/api/hesses`: Create a new hess.
- **GET** `/api/hesses/:id`: Get hess details by ID.
- **PUT** `/api/hesses/:id`: Update hess details by ID.
- **DELETE** `/api/hesses/:id`: Delete a hess by ID.

## Hess Media Upload and Retrieval 📷

- **POST** `/api/hesses/:id/media`: Upload media files (images, videos, audio) to an existing hess.
- **GET** `/api/hesses/:id/media/:id`: Get a hess media file by ID(s).
- **DELETE** `/api/hesses/:id/media/:id`: Delete a hess media file by ID(s).

## Likes ❤️

- **POST** `/api/hesses/:id/like`: Like a hess.
- **DELETE** `/api/hesses/:id/like`: Unlike a hess.

## Feed 📰

- **GET** `/api/feed`: Get the feed.

## Search 🔍

- **GET** `/api/search/hesses`: Search for hesses.
- **GET** `/api/search/users`: Search for users.

## Privacy Preferences 🔒

- **GET** `/api/users/:id/privacy`: Get user's privacy preferences.
- **PUT** `/api/users/:id/privacy`: Update user's privacy preferences.

## Getting Started 🚀

To use this API, follow these steps:

1. Clone this repository to your local machine.
2. Configure the following environment variables.

   ```conf
   # Database Connection
   DATABASE_URL=<your_database_url>

   # JWT Configurations
   JWT_SECRET=<your_jwt_secret>
   JWT_EXPIRE_IN_HOURS=<jwt_expire_time_in_hours>

   # Account Activation Configurations
   ACCOUNT_ACTIVATION_LINK_PREFIX=<account_activation_link_prefix>
   ACCOUNT_ACTIVATION_TOKEN_EXPIRE_IN_HOURS=<activation_token_expire_time_in_hours>

   # Password Reset Configurations
   PASSWORD_RESET_LINK_PREFIX=<password_reset_link_prefix>
   PASSWORD_RESET_TOKEN_EXPIRE_IN_HOURS=<password_reset_token_expire_time_in_hours>

   # Details Included in Emails (you could include only a subset of these)
   FACEBOOK_LINK=<facebook_link>
   TWITTER_LINK=<twitter_link>
   LINKED_IN_LINK=<linkedin_link>
   INSTAGRAM_LINK=<instagram_link>
   FIRST_CONTACT_LINE=<first_contact_line>
   SECOND_CONTACT_LINE=<second_contact_line>
   ```

3. Run the application.
4. Access the API endpoints using the provided routes and methods.

## Contributing 🤝

If you'd like to contribute to this project, feel free to submit pull requests or open issues. Your contributions are greatly appreciated!

## License 📄

This project is licensed under the [MIT License](LICENSE).
