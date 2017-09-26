//used to group distinct  eliment

db.wands.aggregate([
  {"$group":{"_id":"$maker"}}
  
]);

db.wands.aggregate([
  { "$group":{ 
               "_id":"$damage.magic",
               "wand_count":{"$sum":1}
              }
  }
   
]);
