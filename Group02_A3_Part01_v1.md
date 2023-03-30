# General Description of API

## API Description
**How's my prof** is a free online querying tool for professors at the University of Manitoba. Our purpose is to provide information on your past, present, and future instructors using analytics such as faculty, and popularity. We gather our data from the popular **Rate my Professors** as well as the University of Manitoba itself.
## Endpoints & Parameters

**/random**
> Returns a random professor from the University of Manitoba.
- No parameters.

**/faculty/{faculty_name}**
> Returns a list of professors from the specified faculty.
- **faculty_name (string):** Name of the faculty. Required.
- List of accepted input for _faculty_name_:
    - agriculturalandfoodsciences
    - architecture
    - arts
    - business
    - education
    - engineering
    - environmentearthresources
    - extendededucation
    - graduatestudies
    - healthsciences
    - dentalhygiene
    - dentistry
    - medicine
    - nursing
    - pharmacy
    - rehabilitationsciences
    - kinesiologyrecreationmanagement
    - law
    - music
    - science
    - socialwork
    - university1

**/rating/{rating_num}**
> Returns a list of professors that meet the minimum rating of _rating_num_.
- **rating_num (float):** Minimum rating of the professors to be displayed. Valid values are from 0.0 to 5.0. Required.

## Resources
This API has a professor resource which contains name, faculty, and rating attributes. The name attribute contains the name of the professor. The faculty attribute includes the name of the faculty to which the professor belongs. Finally, the rating incorporates the rates for each professor.

```
class ProfessorResource 
    
    attributes :name, :faculty, :rating
    
    # name setter
    def name = (new_name)
        @model.name = new_name
    end
    
    # faculty setter 
    def faculty = (new_faculty)
        @model.faculty = new_faculty
    end
    
    # rating setter
    def rating = (new_rating)
        @model.rating = new_rating
    end
    
    # name getter
    def name 
        @model.name.to_s
    end
    
    # faculty getter
    def faculty 
        @model.faculty.to_s
    end
    
    # rating getter
    def rating
        @model.rating.to_i
    end
end
```

## Sample Requests & Sample Responses
There are three _sample requests_ for getting a professor's rating from our API, they include:    
```
https://api.howsmyprof.org/random  
https://api.howsmyprof.org/faculty/argiculture  
https://api.howsmyprof.org/rating/1.0  
```
The _sample response_ data is formatted in Json, these are the sample responses from the sample requests above respectively:
```
{  
    "results":   
    {  
       "name":"Adam Muller",  
       "faculty":"law",  
       "rating":"3.4"  
    },  
    "status": "success"  
}  

{  
    "results":   
    {  
       "name":"Chris Eliott",  
       "faculty":"agriculture",  
       "rating":"3.4"  
    },    
    {  
       "name":"Yuvrag Gordon",  
       "faculty":"agriculture",  
       "rating":"3.2"  
    },    
    {  
       "name":"Warren Colon",  
       "faculty":"agriculture",  
       "rating":"4.9"    
    }  
    "status": "success"  
}  

{  
    "results":   
    {  
       "name":"Theodore Fulton",  
       "faculty":"music",  
       "rating":"1.0"  
    },  
    "status": "success"  
} 
```
