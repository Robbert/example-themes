# Demodam Hackathon: example theme switcher

**Applying design elements from this project is strictly prohibited for organisations that do not own the respective themes.**

This project is part of a community iniative to use NL Design System design tokens for projects that need to work for multiple organisations and multiple brand guidelines with a shared codebase.

## Mirgatie naar design tokens in CSS met CSS variables

Ga van:

```css
body {
  background-color: white;
  color: black;
}

.btn {
  font-size: 18px;
}

.input {
  border: 1px solid silver;
}
```

Naar:

```css
body {
  background-color: var(--utrecht-document-background-color, white);
  color: var(--utrecht-document-color, black);
}

.btn {
  font-size: var(--denhaag-button-font-size, 18px);
}

.input {
  border-style: solid;
  border-width: 1px;
  border-color: var(--utrecht-textbox-border-color, silver);
}
```

## Eigen design tokens samenstellen

1. Fork deze repository
2. Pas de waardes aan in `design-token-template/`
3. Voer dit script uit om `dist/index.css` te genereren: `npm run build`
4. Maak automatisch `dist/index.css` elke keer als je `*.style-dictionary.json` wijzigt: `npm run watch`
