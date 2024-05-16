# How to deploy an Angular application in Azure
## pokedex (https://pokeferxxo.azurewebsites.net/)


## Creating an APP Service

To deploy the Front-End application, we need to create an “App Service”. In Azure portal, search for “App Services” (this service allows us to deploy our WEB API as software as a service (SaaS):

![Imagen1](https://ferxxostorage.blob.core.windows.net/ferxxo/Img1.jpg "Título opcional")

Then click in “Create”:

![Imagen1](https://ferxxostorage.blob.core.windows.net/ferxxo/img2.jpg "Título opcional")

Now it’s necessary to configure your app service, by selecting your subscription, your resource group, informing a name for the service, the tech stack, operating system, region and the plan:

![Imagen1](https://ferxxostorage.blob.core.windows.net/ferxxo/img3.jpg "Título opcional")


## Build the Angular project created for a deployment in a dev/test environment

Open your terminal or command prompt and run:
```sh
ng build
```
Or
```sh
npm run build
```
If it is a prod project:

```sh
ng build –prod
```

For Angular projects, ng build is the preferred and simplest option, while npm run build is more flexible and suitable for custom scenarios.

![Imagen1](https://ferxxostorage.blob.core.windows.net/ferxxo/img4.jpg "Título opcional")

## Upload dist folder to kudu

Now we look for the next option in our app service where we want to deploy:

![Imagen1](https://ferxxostorage.blob.core.windows.net/ferxxo/img5.jpg "Título opcional")

Inside kudu we go to the next route:

![Imagen1](https://ferxxostorage.blob.core.windows.net/ferxxo/img6.jpg "Título opcional")
In this part we upload our dist folder: 

![Imagen1](https://ferxxostorage.blob.core.windows.net/ferxxo/img7.jpg "Título opcional")

## Change the settings about route mappings in your application service

You must add that name to your default physical path:

changing site\wwwroot => site\wwwroot\dist\pokedex-angular

![Imagen1](https://ferxxostorage.blob.core.windows.net/ferxxo/img8.jpg "Título opcional")
