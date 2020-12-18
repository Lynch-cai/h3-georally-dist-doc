<h3>Metadata</h3>

**Geo**Rally uses conventional HTTP response codes to indicate the success or failure of an API request.

> + Error 200  : Successful  

> + Error 500 : Internal Server Error

``` 
return res.status(500).json({
      statusCode: 500,
      message: 'Internal Server Error',
    })
``` 

``` 
  return res.status(200).json({
    statusCode: 200,
    message: 'Successful',
    data: rows,
  });
``` 