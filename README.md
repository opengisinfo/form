# Form

A lightweight library for building flexible, accessible web forms.

## Documentation

Complete documentation and examples available at [https://form.opengis.info](https://form.opengis.info)

- [Component documentation](https://form.opengis.info/guide/)

## Changelog

Full change log available at [https://form.opengis.info/changelog/](https://iconform.opengis.info/changelog/)

## Install & Usage

### 1. Install
```bash
npm install @opengis/form
```

### 2. Usage

```vue
<template>
  <VsForm
    v-model:form="form"    
    :schema="schema"
    @handle-submit="handleSubmit"
  />
</template>

<script setup>
  import { ref } from 'vue';
  import { VsForm } from "@opengis/form";
  
  const form = ref({});
  const formValues = ref({});

  const schema = [
    {
      name: 'name',
      type: 'text',
      label: 'Full Name',
      placeholder: 'Enter your full name',
      rules: ['required'],
    },
    {
      name: 'email',
      type: 'text',
      label: 'Email',
      placeholder: 'Enter your email',
      rules: ['required', 'email'],
    },
    {
      name: 'country',
      type: 'select',
      label: 'Country',
      options: [
        { id: 'ua', text: 'Ukraine' },
        { id: 'us', text: 'United States' },
      ],
      rules: ['required'],
    },
  ];

  const handleSubmit = values => {
    console.log('Form submitted:', values);
  };
</script>
```

## Contributions
We welcome contributions!
Feel free to open issues, suggest features, or submit pull requests.

## Licence

MIT
