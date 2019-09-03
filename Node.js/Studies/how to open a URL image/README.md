# How to open a url image 
This folder shows the steps to open a image by url in Node.js.

## Step 01
Create a url attribute in the model that you want the url image.
	url: {
          type: Sequelize.VIRTUAL,
          get() {
            return `${process.env.APP_URL}/files/${this.path}`; // this return the path to open your image
          },
        },


## Step 02
Now create a middleware to intercept all the url requests.
Add this middleware inside your app.js file in middleware method.

```bash
this.server.use(
  '/files',
  express.static(path.resolve(__dirname, '..', 'tmp', 'uploads'))
);
```



