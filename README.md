
This package will help you to automatically link all occurrences of
your term words within given text. Great for SEO and stuff.

## Usage

### 1. Install the package

```
composer require psmb/term
```

### 2. Add `Psmb.Term:TermMixin` to the nodetypes that you want to use as terms

```
'Your.NodeTypes:Tag':
  superTypes:
    'Psmb.Term:TermMixin': true
```

### 3. Process any text you want with `Psmb.Term:ReplaceTerms` TS object

E.g. if you want terms to be replaced in all Text nodes:

```
prototype(TYPO3.Neos.NodeTypes:Text) {
	text.@process.replaceTags = Psmb.Term:ReplaceTerms
}
```

### 4. Create term nodes

You may also fill-in their `replaceVariants` property for alternative spelling variants
