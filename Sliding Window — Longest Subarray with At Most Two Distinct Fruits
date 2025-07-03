/**
 * @param {number[]} fruits
 * @return {number}
 */
var totalFruit = function(fruits) {
    let left = 0;
    let maxFruits = 0;
    let basket = {};
    let fruitTypes = 0;

    for(let right = 0; right < fruits.length; right++){
        let currentFruit = fruits[right];

        if(basket[currentFruit] === undefined){
            basket[currentFruit] = 1;
            fruitTypes++;
        }else{
            basket[currentFruit]++;
        }

        while(fruitTypes > 2){
            let leftFruit = fruits[left];
            basket[leftFruit]--;

            if(basket[leftFruit] === 0){
                delete basket[leftFruit];
                fruitTypes--;
            }
            left++;
        }
        let currentWindowSize = right - left + 1;
        if(currentWindowSize > maxFruits){
            maxFruits = currentWindowSize;
        }
    }
    return maxFruits;
};