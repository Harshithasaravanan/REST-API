const Item = require('../models/itemModel');

exports.getAllItems = async (req, res) => {
  try {
    const items = await Item.find();
    res.json(items);
  } catch (error) {
    res.status(500).json({ error: 'An error occurred' });
  }
};

exports.createItem = async (req, res) => {
  try {
    const newItem = new Item({ name: req.body.name });
    await newItem.save();
    res.status(201).json(newItem);
  } catch (error) {
    res.status(500).json({ error: 'An error occurred' });
  }
};
