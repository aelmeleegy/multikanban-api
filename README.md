multikanban
===========

A simple kanban for multiple personal projects.


# Request & Response Examples

## API Resources

### USERS

| Endpoint | Description |
| ---- | --------------- |
| [POST /users](#post-users) | Create a user |
| [GET /users](#get-users) | Get all users |
| [GET /users/:id](#get-user) | Get a user data |
| [PUT /users/:id](#put-user) | Update user's data |
| [DELETE /users/:id](#delete-user) | Delete user |
  
### KANBANS
  
| Endpoint | Description |
| ---- | --------------- |
| [POST /users/:id/kanbans](#post-kanbans) | Create a kanban for user :id |
| [GET /users/:id/kanbans](#get-kanbans) | Get all kanbans from user :id |
| [GET /users/:id/kanbans/:kanban_id](#get-kanban) | Get kanban :kanban_id from user :id |
| [PUT /users/:id/kanbans/:kanban_id](#put-kanban) | Update kanban :kanban_id from user :id |
| [DELETE /users/:id/kanbans](#delete-kanbans) | Delete all kanbans from user :id |
| [DELETE /users/:id/kanbans/:kanban_id](#delete-kanban) | Delete kanban :kanban_id from user :id |

### TASKS

| Endpoint | Description |
| ---- | --------------- |
| [POST /users/:id/kanbans/:kanban_id/tasks](#post-tasks) | Create a task in kanban :kanban_id of user :id |
| [GET /users/:id/kanbans/:kanban_id/tasks](#get-tasks) | Get all tasks from kanban :kanban_id from user :id |
| [GET /users/:id/tasks](#get-all-tasks) | Get all tasks from user :id ?????????????? |
| [PUT /users/:id/kanbans/:kanban_id/tasks/:task_id](#put-task) | Update task :task_id from kanban :kanban_id from user :id |
| [DELETE /users/:id/tasks](#delete-tasks) | Delete all tasks from user :id |
| [DELETE /users/:id/kanbans/:kanban_id/tasks/:task_id](#delete-task) | Delete task :task_id from kanban :kanban_id from user :id |


* I need a call to retrieve the total number of:
 - users
 - kanbans
 - kanbans per user
 - tasks
 - tasks per user
 - completed tasks (done + archive)
 - completed tasks (done + archive) per user
 

#### GET /users

Example: http://multikanban.com/api/users.json

Response body:

    {
        "metadata": {
            "count": 123,
        },
        "results": [
            {
                "id": "1",
                "nickname": "mezod",
                "registered": "31/08/2014",
                "numberkanbans": "7",
            },
            {
                "id": "2",
                "nickname": "cowboycoder",
                "registered": "31/08/2014",
                "numberkanbans": "3",
            },
            {
                "id": "3",
                "nickname": "gravitysrainbow",
                "registered": "31/08/2014",
                "numberkanbans": "4",
            },

        ]
    }
