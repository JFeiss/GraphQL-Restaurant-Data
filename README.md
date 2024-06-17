# GraphQL-Restaurant-Data
<img src= "Screenshot 1restaurant.png" width='300'/>

GraphQL restaurant Data - query and mutations to  perform CRUD operations
run https://localhost:5500/graphQL<br>

mutation editrestaurant($idd: Int = 1, $name: String = "OLDO") {
  editrestaurant(id: $idd, name: $name) {
    name
    description
  }
}

mutation setrestaurant {
  setrestaurant(input: {name: "Granite", description: "American"}) {
    name
    description
  }
}

mutation deleterestaurant($iid: Int = 1) {
  deleterestaurant(id: $iid) {
    ok
  }
}

query restaurant($iid: Int = 1) {
  restaurant(id: $iid) {
    name
    description
  }
}

query getrestaurants {
  restaurants {
    name
    description
    dishes {
      name
      price
    }
  }
}


