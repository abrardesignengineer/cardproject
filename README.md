# CSS Notes: Positioning and Box Sizing

## 1. `box-sizing: border-box`

Includes padding and borders inside the specified width and height.

```css
.profile-card {
  width: 400px;
  height: 400px;
  padding: 20px;
  box-sizing: border-box;
}
```

The total dimensions remain 400px × 400px, including padding and borders.

Without `border-box`, the default `content-box` adds padding and borders outside the specified dimensions.

## 2. `left: 50%`

Moves an absolutely positioned element so its left edge is at 50% of its containing block's width.

```css
.avatar {
  position: absolute;
  left: 50%;
}
```

This does not center the element itself. Its left edge is at the midpoint.

## 3. `transform: translateX(-50%)`

Moves the element left by 50% of its own width.

```css
.avatar {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
}
```

Combining these properties centers the avatar horizontally within its positioning reference.

## Key takeaway

- `left: 50%` uses the containing block as the reference.
- `translateX(-50%)` uses the element's own width as the reference.
- `box-sizing: border-box` includes padding and borders in the specified dimensions.
