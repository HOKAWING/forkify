# forkify
功能：选择食品，查看详情，添加喜欢。

<img src="/image/pic.png" width="900px" />

素材来自于网站https://www.udemy.com/the-complete-javascript-course/learn/v4/content

1. data-  
/**  
    data-goto属性：(goto是自定义的名字)  
    Whenever we prefix an attribute with data, then this variable here gets stored in a dataset dot.  
    You can use 'btn.dataset.goto' to get values, This is very handy way of having access to data.  
*/

2. Parameter default value.  
export const limitRecipeTitle = (title, limit = 17) => {  

3. Persist data in localStorage.  
    persistData() {  
        //保存在browser sessions中，重新刷新页面或重啟電腦也存在 . 
        /**  localStorage is similar to sessionStorage, except that while data stored in localStorage has no expiration time, data stored in sessionStorage gets cleared when the page session ends.
        */  
        localStorage.setItem('likes', JSON.stringify(this.likes));  
    }  
    readStorage() {  
        const storage = JSON.parse(localStorage.getItem('likes'));  
    }

4. Get recipe from external API.  
    import axios from 'axios';  
    const res = await axios(`https://www.food2fork.com/api/get?key=${key}&rId=${this.id}`);  
    this.title = res.data.recipe.title;  
    
5. join array.  
        const unitsShort = ['tbsp', 'tbsp', 'oz', 'oz', 'tsp', 'tsp', 'cup', 'pound'];  
        const units = [...unitsShort, 'kg', 'g'];  
        
