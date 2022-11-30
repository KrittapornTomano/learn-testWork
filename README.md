const dog = {
    name:'me',
    breed:'aaa',
    breed2:'aazxczxa',
    breed3:'aasadsda'
    
    
}

    const fs = require('fs')

    const saveData = (dog) =>{
        const finished = (error) =>{
            if(error){
                console.error(error)
                return;
            }
        }

        const jsonData =JSON.stringify(dog,null,2)
        fs.writeFile('data.json',jsonData,finished)

    }

    saveData(dog)
