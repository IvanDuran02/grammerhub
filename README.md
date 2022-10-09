This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.js`. The page auto-updates as you edit the file.

## Endpoints:
CityFi base url: 

- all endpoints are public access, no restrictions

## [GET]: api/user/users

get all users

- return JSON format:
    
    ```jsx
    {
        "users": [
            {
                "id": 3,
                "name": "guest",
                "email": "guest@cityfi.gov",
                "role": "guest"
            },
            {
                "id": 15,
                "name": "user1",
                "email": "user1@cityfi.gov",
                "role": "user"
            }
        ]
    }
    ```
    
- 

## [GET]: api/report/reports

get all reports

- return JSON format:

```jsx
{
    "reports": [
        {
            "id": 6,
            "authorId": 3,
            "createdAt": "2022-10-09T09:03:36.975Z",
            "updatedAt": "2022-10-09T09:03:36.975Z",
            "status": "pending",
            "latitude": 26.3749876,
            "longitude": -80.103252,
            "category": "residential",
            "subCategory": "",
            "description": "coconuts everywhere!"
        },
        {
            "id": 7,
            "authorId": 15,
            "createdAt": "2022-10-09T09:56:21.759Z",
            "updatedAt": "2022-10-09T09:56:21.759Z",
            "status": "pending",
            "latitude": 26.3749876,
            "longitude": -80.103252,
            "category": "hazards",
            "subCategory": "park & rec",
            "description": "trash bins are full everywhere"
        }
    ]
}
```

## [GET]: api/report/[id]

get report by id

- return JSON format:
    
    ```jsx
    {
        "id": 6,
        "authorId": 3,
        "createdAt": "2022-10-09T09:03:36.975Z",
        "updatedAt": "2022-10-09T09:03:36.975Z",
        "status": "pending",
        "latitude": 26.3749876,
        "longitude": -80.103252,
        "category": "residential",
        "subCategory": "",
        "description": "coconuts everywhere!"
    }
    ```
    

## [GET]: api/user/[id]

get user by id

- return JSON format:

```jsx
{
    "id": 3,
    "name": "guest",
    "email": "guest@cityfi.gov",
    "role": "guest"
}
```

## [POST]: api/report/create-report

create a new report

- return JSON format:

```jsx
{
    "newReport": {
        "id": 8,
        "authorId": 15,
        "createdAt": "2022-10-09T11:01:52.525Z",
        "updatedAt": "2022-10-09T11:01:52.525Z",
        "status": "pending",
        "latitude": 26.3749876,
        "longitude": -80.103252,
        "category": "hazards",
        "subCategory": "park & rec",
        "description": "new reporting for the city"
    },
    "message": "Report# 8 was successfully created!"
}
```

## [POST]: api/user/create-user

create a new user

- return JSON format:

```jsx
{
    "newUser": {
        "id": 19,
        "name": "user2",
        "email": "user2@cityfi.gov",
        "role": "user"
    },
    "message": "user user2 was successfully created!"
}
```

## [DELETE]: api/report/[id]

delete report by id

- return message:

```jsx
"report id #7 has been successfully deleted"
```

## [DELETE]: api/user/[id]

delete user by id

- return JSON format:

```jsx
{
    "deleteUser": {
        "id": 19,
        "name": "user2",
        "email": "user2@cityfi.gov",
        "role": "user"
    },
    "message": "user user2 has been successfully deleted"
}
```

## [PUT]: api/report/[id]

update report by id

- return JSON format

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
