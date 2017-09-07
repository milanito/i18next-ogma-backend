# i18next-ogma-backend

This is a simple i18next backend to be used when you have a [ogma](https://github.com/milanito/ogma) instance.

## Getting started

Source can be installed doing this :

    $ npm install i18next-ogma-backend
    $ yarn add i18next-ogma-backend

Using it then is quite straightfoward :

    import i18next from 'i18next';
    import ogmaBackend from 'i18next-ogma-backend';

    i18next
    .use(ogmaBackend)
    .init(i18nextOptions)

## Backend Options

The following options are available :

```
{
  // Your backend URL
  url: 'https://some.url',
  id: 'your client id',
  token: 'your client secret',
}
```

Please pass the options using the preferred way, using the `i18next.init`.

    import i18next from 'i18next';
    import ogmaBackend from 'i18next-ogma-backend';

    i18next
    .use(ogmaBackend)
    .init({
      backend: options,
      ...
    })

You can also use the other methods :

    import ogmaBackend from 'i18next-ogma-backend';

    // construction
    const instance = new ogmaBackend(null, options);
    // or init
    const instance = new ogmaBackend();
    instance.init(options);

## License

MIT
