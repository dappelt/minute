# Minute
> Support content creators with ILP

- [Quick Start](#quick-start)
- [Enable your Site](#enable-your-site)

## Quick Start

Before you use this module, install and run [Moneyd](https://github.com/sharafian/moneyd).

```sh
git clone https://github.com/sharafian/minute.git
cd minute
npm install
npm run build
```

Now go to `chrome://extensions`, tick the checkbox "Developer mode", select "Load unpacked extension", and nagivate
to the folder where you cloned this repository.

## Enable your Site

Add the following tag to your site's body:

```html
<script>
  if (ILP && ILP.pay) {
    ILP.pay({
      receiver: /* Put your SPSP payment pointer here */
    }).then(paying => {
      // Make sure to thank the user!
    })
  }
</script>
```

Now any user who navigates to your site and has Minute enabled will stream
payments to you. Thanking your supporters and offering them a premium
experience will incentivise them to come back.
