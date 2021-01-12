## Run the application

npm install

After that 

npm start

## GRAPHQL Queries

 -> get All users

 query {
  users {
    id
  	firstname
    lastname
    nickname
    email
    password
  }
}

-> get user by ID

query {
  user(id: "2") {
    id
    firstname
    lastname
    nickname
    email
    password
  }
}

-> Create User 

mutation {
  createUser(
    data: {
      firstname: "Micheal",
      lastname: "Daralola",
      nickname: "Gelgit",
      email: "michaeldaralola123@gmail.com",
      password: "hackme"
    }
  ) {
    id
    firstname
    lastname
    nickname
    email
    password
  }
}

-> update user

mutation {
  updateUser(
    id: "2", 
    data: {
    	nickname: "Dumbo"
  	}
  )
  {
    id
    firstname
    lastname
    nickname
    email
    password
  }
}

-> Delete User

mutation {
  deleteUser(id: "3")
}



