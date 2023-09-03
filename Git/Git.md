**Solution**:

```javascript
function maxArea(height) {
    let left = 0;
    let right = height.length - 1;
    let maxWater = 0;

    while (left < right) {
        let minHeight = Math.min(height[left], height[right]);
        let width = right - left;
        maxWater = Math.max(maxWater, minHeight * width);

        if (height[left] < height[right]) {
            left++;
        } else {
            right--;
        }
    }

    return maxWater;
}
```

---

**Problem Explanation**:

Imagine `n` vertical lines standing on the x-axis. Each line's height is given by the `height` array. The goal is to find two lines such that the area they form with the x-axis (as the base) is maximized. This area will be the maximum amount of water the container can hold. The challenge is to find the pair of lines that maximize this area.

**Solution Explanation**:

1. **Two Pointers**: We begin with two pointers, `left` and `right`, initialized at the beginning and end of the `height` array.
2. **Calculate Area**: At each step, calculate the area using the shorter line's height (either the one pointed to by `left` or `right`) and the distance between the two pointers (which will be the width of the container). Update `maxWater` if the calculated area is greater than the current `maxWater`.
3. **Move Pointers**: Move the pointer that is pointing to the shorter line. The rationale behind this is simple: if we move the taller line, the height for our container doesn't increase (it's determined by the shorter line), but the width will decrease (since we are moving the pointers closer). Thus, moving the taller line will not help in maximizing the area. The only option left is to move the shorter line and hope for a taller line in its direction.
4. **Return**: Continue the process until the `left` pointer is less than the `right` pointer. After the loop, `maxWater` will have the maximum area (or the maximum amount of water the container can hold).

This solution is efficient and runs in linear time since we process each line only once.