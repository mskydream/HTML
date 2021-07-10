# Fragmentation

## Media print page-break

```css
@media print{
	p{
		page-break-inside: avoid;
	}
	h1{
		page-break-before: always;
	}
	h2{
		page-break-after: avoid;
	}
}
```

