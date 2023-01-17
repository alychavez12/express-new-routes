
# mount routes

## Main page

 * app.get('/', function (req, res) {
     console.log('index route is working)
      res.redirect('/fruits');

## Index- GET /fruits

   * app.get('/fruits', function (req, res) {
     res.render('index.ejs', {
       Fruits: fruits
  });

## New- GEt/fruits/new - send the user to a new page 

  * app.get('/fruits/new', function (req, res) {
       Res.render('new.ejs');
 });

## Delete- 

  * app.delete('/pokemon/:indexOfFruitsArray', function (req, res) {
    fruits.splice(req.params.indexOfFruitsArray, 1);
    res.redirect('/fruits');
});
 
## Update-

 * app.put('/fruits/:indexOfFruitsArray', function (req, res) {
    fruits[req.params.indexOfFruitsArray] = req.body;
    res.redirect('/fruits');
});

## Create- POST /fruits - take form data and create a new route with it

 * app.post('/fruits', function (req, res) {
    fruits.push(req.body);
    res.redirect('/fruits');
});

## Edit- GET request /fruits/:indexOfArray/edit - sending a page that allow to edit the fruit

  * app.get('/fruits/:indexOfFruitsArray/edit', (req, res) => {
    res.render(
        'edit.ejs', {
            fruit: fruits[req.params.indexOfFruitsArray],
            index: req.params.indexOfFruitsArray,
        }
    );
});

* Show- GET /fruits/:someUniqueIdentifier

 app.get('/fruit/:indexOfFruitsArray', function (req, res) {
    const fruit = fruis[req.params.indexOfFruitsArray];
    res.render('show.ejs', {
        fruit: fruit
    });
});
