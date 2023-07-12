# bookshelf-api

1. Folder ini hanya untuk backend dengan pengujian API Automation POSTMAN
2. Buka VSCODE dan import seluruh folder 'bookshelf-api'
3. Silahkan install dependecies : @hapi/hapi, @nanoid3, nodemon
4. Kemudian buka terminal dan masuk ke folder bookshelf-api
5. Start server dengan syntax : 'npm run start-dev'
6. Pastikan keluar hasil : 'http://localhost:9000'
7. Buka POSTMAN dan buat intruksi untuk POST, GET, PUT, DELETE
8. POST : http://localhost:9000/books dengan body raw json
   {
    "id": "Qbax5Oy7L8WKf74l",
    "name": "Buku A",
    "year": 2010,
    "author": "John Doe",
    "summary": "Lorem ipsum dolor sit amet",
    "publisher": "Dicoding Indonesia",
    "pageCount": 100,
    "readPage": 25,
    "finished": false,
    "reading": false,
    "insertedAt": "2021-03-04T09:11:44.598Z",
    "updatedAt": "2021-03-04T09:11:44.598Z"
}
9. GET : http://localhost:9000/books dengan response body seharusnya
    {
    "status": "success",
    "data": {
        "books": [
            {
                "id": "Qbax5Oy7L8WKf74l",
                "name": "Buku A",
                "publisher": "Dicoding Indonesia"
            },
   
        ]
    }
}
10. GET : http://localhost:9000/books/id dengan response body seharusnya
    {
    "status": "success",
    "data": {
        "book": {
            "id": "Qbax5Oy7L8WKf74l",
            "name": "Buku A",
            "year": 2011,
            "author": "Jane Doe",
            "summary": "Lorem Dolor sit Amet",
            "publisher": "Dicoding Indonesia",
            "pageCount": 200,
            "readPage": 26,
            "finished": false,
            "reading": false,
            "insertedAt": "2021-03-05T06:14:28.930Z",
            "updatedAt": "2021-03-05T06:14:30.718Z"
        }
    }
}
11. PUT : http://localhost:9000/books/id dengan response body seharusnya
    {
    "status": "success",
    "message": "Buku berhasil diperbarui"
}
12. DEL : http://localhost:9000/books/id dengan response body seharusnya
    {
    "status": "success",
    "message": "Buku berhasil dihapus"
}
