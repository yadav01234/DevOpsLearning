**The Search for the Mightiest Reservoir**

In a bustling city named Arrayville, there were numerous magnificent pillars, each of varying height, planted on a vast stretch of land. The pillars stood in a straight line, and each was assigned an index, starting from 0 to n-1. The taller the pillar, the higher its prominence on the horizon. The height of these pillars is given by the array `height`.

Two architects, Left and Right, were assigned a task: to select two pillars and design a magnificent reservoir between them to hold rainwater. This reservoir would be bound by the x-axis below, and the two pillars on the sides.

1. **Setting their initial positions:**
   ```javascript
   let left = 0;
   let right = height.length - 1;
   ```
   Left began at the very first pillar (index 0) and Right at the very last pillar.

2. **Hunting for the maximum water storage:** 
   They had a measuring tape, `maxWater`, which would note down the largest reservoir size they've found so far.
   ```javascript
   let maxWater = 0;
   ```

3. **The journey and evaluation:**
   Left and Right began examining the spaces between pillars:
   ```javascript
   while (left < right) {
   ```
   They would measure the distance (or width) between them and use the shorter pillar's height (since water would spill over the shorter pillar).
   ```javascript
       let minHeight = Math.min(height[left], height[right]);
       let width = right - left;
       maxWater = Math.max(maxWater, minHeight * width);
   ```

4. **Decision-making:**
   If the pillar where Left stood was shorter than where Right was, Left would move to the next pillar. Otherwise, Right would move one pillar towards Left. They hoped this strategy would increase the potential reservoir's volume.
   ```javascript
       if (height[left] < height[right]) {
           left++;
       } else {
           right--;
       }
   ```

Finally, after assessing all potential reservoirs, they had the size of the mightiest one stored in `maxWater`.

And thus, using their wisdom and the mighty power of mathematics, Left and Right found the space between two pillars that could form the largest reservoir in Arrayville.