const { page } = req.query; // Here you need to create a query param to get the page

const appointments = await Appointment.findAll({
      where: {
        user_id: req.userId,
        canceled_at: null,
      },
      order: ['date'], // Order by date
      attributes: ['id', 'date'], 

      // PAGINATION EXAMPLE:
      limit: 20, // limit of 20 rows inside a page
      offset: (page - 1) * 20, // return the number of pages * 20
}
