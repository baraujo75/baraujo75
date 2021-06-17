### Hi there 👋


- 📫 How to reach me: bruno.bvaraujo@gmail.com


 const fetcher = (variables, token) => { 
   return request( 
     { 
       query: ` 
       query userInfo($login: String!) { 
         user(login: $login) { 
           repositories(isFork: false, first: 100) { 
             nodes { 
               languages(first: 1) { 
                 edges { 
                   size 
                   node { 
                     color 
                     name 
                   } 
                 } 
               } 
             } 
           } 
         } 
       } 
