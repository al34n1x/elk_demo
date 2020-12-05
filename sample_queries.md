# Add index

PUT /index_mcu/avengers/6

{
    "name": "IronMan",
    "interest":"Technology"
}


# Get index

GET /index_MCU/Avengers/6


# Update index

POST /index_MCU/Avengers/6/_update

{
    "doc":{"interest":"Nano Technology"}

}

# DSL

POST /index_mcu/avengers/_search

{
    "query": {

        "match_all":{}
    }

}


GET /index_mcu/avengers/_search
{
  "query": {
    "match": {
      "name": "Ironman"
    }
  }
}


# Sample Data eCommerce


GET kibana_sample_data_ecommerce/_search
{
  "query":{
    "match":{
      "customer_first_name": "Eddie"
    }
  }
}

POST kibana_sample_data_ecommerce/_doc/0E3uMHYBFndMxx1ioI1I/_update
{
  
  "doc":{"customer_first_name":"Ed"}
  
}

GET kibana_sample_data_ecommerce/_doc/0E3uMHYBFndMxx1ioI1I




