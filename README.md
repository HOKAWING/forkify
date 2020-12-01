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
        //保存在内存中，重新刷新页面也存在。
        localStorage.setItem('likes', JSON.stringify(this.likes));
    }
    readStorage() {
        const storage = JSON.parse(localStorage.getItem('likes'));
    }
