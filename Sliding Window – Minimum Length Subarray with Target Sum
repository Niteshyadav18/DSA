/**
 * @param {number} target
 * @param {number[]} nums
 * @return {number}
 */
var minSubArrayLen = function(target, nums) {
    let left = 0;
    let currentSum = 0;
    let minSize = Infinity;

    for(let right = 0; right < nums.length; right++){
        currentSum += nums[right];

        while(currentSum >= target){
            let windowSize = right - left + 1;
            minSize = Math.min(minSize, windowSize);
            currentSum -= nums[left];
            left++;
        }
    }
    return minSize === Infinity ? 0 : minSize;
};
