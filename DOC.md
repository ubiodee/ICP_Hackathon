# Backend Actor Documentation

This `Backend` actor provides various functionalities for managing profiles, posts, comments, likes, and bookmarks in a social media-like application.

## Table of Contents

- [Profile Management](#profile-management)
    - [createProfile](#createprofile)
    - [updateProfile](#updateprofile)
    - [getProfileWithUsername](#getprofilewithusername)
    - [getProfileWithPrincipal](#getprofilewithprincipal)
- [Post Management](#post-management)
    - [addPost](#addpost)
    - [updatePost](#updatepost)
    - [deletePost](#deletepost)
    - [getAllPosts](#getallposts)
    - [getAllUsersPosts](#getallusersposts)
    - [getPostById](#getpostbyid)
- [Comment Management](#comment-management)
    - [addComment](#addcomment)
    - [deleteComment](#deletecomment)
- [Like Management](#like-management)
    - [addLike](#addlike)
    - [removeLike](#removelike)
    - [getLikesForPost](#getlikesforpost)
- [Bookmark Management](#bookmark-management)
    - [bookmarkAPost](#bookmarkapost)
    - [removefromBookmark](#removefrombookmark)
    - [getBookmarks](#getbookmarks)
- [Keyword Search](#keyword-search)
    - [getPostsByKeyWord](#getpostsbykeyword)

## Profile Management

### `createProfile`

Creates a new profile for the caller.

- **Parameters:**
    - `_username`: The username for the profile.
    - `_bio`: The biography of the user.
    - `_socials`: A list of social media links associated with the profile.
- **Returns:** The newly created `Profile`.

### `updateProfile`

Updates the profile of the caller with new information.

- **Parameters:**
    - `_prof`: An object containing the new `username`, `bio`, and `socials` for the profile.
- **Returns:** The updated `Profile`.

### `getProfileWithUsername`

Retrieves a profile using the username.

- **Parameters:**
    - `_username`: The username associated with the profile.
- **Returns:** An optional `Profile` if found, otherwise `null`.

### `getProfileWithPrincipal`

Retrieves a profile using the principal.

- **Parameters:**
    - `_principal`: The principal associated with the profile.
- **Returns:** An optional `Profile` if found, otherwise `null`.

## Post Management

### `addPost`

Adds a new post for the caller.

- **Parameters:**
    - `_title`: The title of the post.
    - `_body`: The content of the post.
    - `_externalLinks`: A list of external links related to the post.
    - `_keywords`: A list of keywords associated with the post.
- **Returns:** The newly created `Post`.

### `updatePost`

Updates an existing post.

- **Parameters:**
    - `_id`: The ID of the post to be updated.
    - `_title`: The new title for the post.
    - `_body`: The updated content of the post.
    - `_externalLinks`: A list of updated external links.
    - `_keywords`: A list of updated keywords.
- **Returns:** The updated `Post`, or `null` if the post does not exist.

### `deletePost`

Deletes a post by its ID.

- **Parameters:**
    - `_id`: The ID of the post to delete.
- **Returns:** The deleted `Post`, or `null` if the post does not exist.

### `getAllPosts`

Retrieves a list of posts with pagination.

- **Parameters:**
    - `_start`: The starting index for pagination.
    - `_length`: The number of posts to retrieve.
- **Returns:** A list of `Post` objects.

### `getAllUsersPosts`

Retrieves all posts or comments by a specific user with pagination.

- **Parameters:**
    - `_author`: The username of the author whose posts or comments to retrieve.
    - `_start`: The starting index for pagination.
    - `_length`: The number of posts or comments to retrieve.
    - `_isPost`: A boolean indicating if the query is for posts (true) or comments (false).
- **Returns:** A list of post or comment IDs.

### `getPostById`

Retrieves a specific post or comment by its ID.

- **Parameters:**
    - `_id`: The ID of the post or comment to retrieve.
    - `_isPost`: A boolean indicating if the query is for a post (true) or a comment (false).
- **Returns:** The `Post` or `Comment` if found.

## Comment Management

### `addComment`

Adds a comment to a post or another comment.

- **Parameters:**
    - `_to`: The ID of the post or comment being commented on.
    - `_body`: The content of the comment.
    - `_underPost`: A boolean indicating if the comment is under a post (true) or another comment (false).
- **Returns:** The newly created `Comment`.

### `deleteComment`

Deletes a comment by its ID.

- **Parameters:**
    - `_id`: The ID of the comment to delete.
- **Returns:** The deleted `Comment`, or `null` if the comment does not exist.

## Like Management

### `addLike`

Adds a like to a post or comment.

- **Parameters:**
    - `_to`: The ID of the post or comment being liked.
    - `_underPost`: A boolean indicating if the like is for a post (true) or a comment (false).
- **Returns:** A list of usernames who have liked the post or comment.

### `removeLike`

Removes a like from a post or comment.

- **Parameters:**
    - `_id`: The ID of the like to remove.
- **Returns:** A list of usernames who have liked the post or comment after removal, or `null` if the like does not exist.

### `getLikesForPost`

Retrieves a list of likes for a specific post or comment.

- **Parameters:**
    - `_id`: The ID of the post or comment.
    - `_isPost`: A boolean indicating if the query is for a post (true) or a comment (false).
- **Returns:** A list of usernames who have liked the post or comment.

## Bookmark Management

### `bookmarkAPost`

Bookmarks a post for the caller.

- **Parameters:**
    - `_id`: The ID of the post to bookmark.
- **Returns:** A list of post IDs that the caller has bookmarked.

### `removefromBookmark`

Removes a post from the caller's bookmarks.

- **Parameters:**
    - `_id`: The ID of the post to remove from bookmarks.
- **Returns:** A list of post IDs remaining in the caller's bookmarks.

### `getBookmarks`

Retrieves the list of bookmarked posts for a specific user.

- **Parameters:**
    - `_principal`: The principal of the user.
- **Returns:** An optional list of bookmarked post IDs.

## Keyword Search

### `getPostsByKeyWord`

Retrieves posts associated with a specific keyword.

- **Parameters:**
    - `_keyword`: The keyword to search for.
    - `_start`: The starting index for pagination.
    - `_length`: The number of posts to retrieve.
- **Returns:** A list of post IDs associated with the keyword.
