```
function maxArea(height) {
    //set the start and end points.
    let left = 0;
    let right = height.length - 1;
    // at first maximum water will be 0
    let maxWater = 0;

    // run the loop from the starting and check each pillar.
    while (left < right) {
        // calculations for max water.
        let minHeight = Math.min(height[left], height[right]);
        let width = right - left;
        maxWater = Math.max(maxWater, minHeight * width);

        // once calculation is done , update the loop variables.
        //take care so you dont enter into a infinte loop.
        if (height[left] < height[right]) {
            left++;
        } else {
            right--;
        }
    }
    // return the result back.
    return maxWater;
}
```