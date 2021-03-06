---
title: Animation
codeSandboxId: 31VMyP7XO
---

Pour faire de l'animation avec glamorous, vous pouvez utiliser pour des choses simples
des transitions CSS ordinaires et pour des choses plus avancées, vous pouvez utiliser `keyframes`
via l'API `css.keyframes` de glamour.

```interactive
// import * as glamor from 'glamor'

// Définit les styles de l'animation
const animationStyles = props => {
  const bounce = glamor.css.keyframes({
    '0%': { transform: `scale(1.01)` },
    '100%': { transform: `scale(0.99)` }
  })
  return {animation: `${bounce} 0.2s infinite ease-in-out alternate`}
}

// Definit l'élément
const AnimatedDiv = glamorous.div(animationStyles)

render(
  <AnimatedDiv>
    Bounce.
  </AnimatedDiv>
)
```
