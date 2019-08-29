* You need to create a new middleware to open a url image
Example:
	middlewares() {
	    this.server.use(express.json());
	    // Method necessary to open urls files
	    this.server.use(
	      '/files',
	      express.static(path.resolve(__dirname, '..', 'tmp', 'uploads')) // pass the path where your imgs are storage
	    );
	  } 


// Example of a index method
async index(req, res) {
    const providers = await User.findAll({
      where: { provider: true },
      attributes: ['id', 'name', 'email', 'avatar_id'], // Only return the specified attributes
      include: [
        // Include the json file
        {
          model: File,
          as: 'avatar',
          attributes: ['name', 'path', 'url'],
        },
      ],
    });
