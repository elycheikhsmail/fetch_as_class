# fetch_as_class
class for fetch data based on fetch api
example 
```
//sava as my.test.ts
// deno run  --location http://localhost:8080 my.test.ts
import {  FetchHelper  } from "https://deno.land/x/fetch_as_class@v1.0.5/mod.ts";
const fetchHepler = new FetchHelper();
import * as t from "https://deno.land/std@0.102.0/testing/asserts.ts";


Deno.test(
    "test 1 for get list domain ",
    async () => { 
      fetchHepler.setPathname("/api/todos");    
      const response = await fetchHepler.GET() 
      t.assertEquals(response.status, 200); 
    },
  );
  


```
