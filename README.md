# Javascript-Promise

A Javascript `Promise` is a representation of a value/data that is still to be.

* `Producing Code`:

Code that is responsible for getting the required values/data

* `Consuming Code`:

Code that must wait for the producer to deliver the required data to be consumed or perform the defined data manipulations

A `Promise` is a Javascript object that links producing and consuming code.

```
const productionWasSuccessful = false;

const producer = new Promise((resolver, rejector) => {
  const package = { message: "I'm the package that was promised" };
  const deliveryIssue = { message: "The package could not be delivered production failed" };

  productionWasSuccessful ? resolver(package) : rejector(deliveryIssue);
});

producer.then((data) => console.log(data.message)).catch((error) => console.log(error.message));
```

