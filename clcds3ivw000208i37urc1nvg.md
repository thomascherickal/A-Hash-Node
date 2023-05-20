---
title: "Part 2: How to Code with ChatGPT"
seoTitle: "How to Create s DDD CRUD application in F# with two sentences"
seoDescription: "This is going to change the world!"
datePublished: Sun Jan 01 2023 19:41:28 GMT+0000 (Coordinated Universal Time)
cuid: clcds3ivw000208i37urc1nvg
slug: part-2-how-to-code-with-chatgpt
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1672602027809/ec7572fd-d984-47f6-8135-4533fa42f95d.png
tags: automation, deep-learning, chatgpt, nlp-transformers

---

(continued from Medium)

Create with source code and database A DDD CRUD Application with external database SQL Server in [F#.NET](http://F#.NET).

Answer:

*Sure! Here's an example of how you can create a DDD CRUD application with an external SQL Server database in* [*F#.NET*](http://F#.NET)*.*

*First, you will need to install the necessary dependencies. You can do this using the .NET CLI by running the following command:*

```plaintext
dotnet add package Microsoft.EntityFrameworkCore
dotnet add package Microsoft.EntityFrameworkCore.SqlServer
```

*Next, you will need to define your domain model. For example, let's say you have a* `Product` *entity with the following properties:*

```plaintext
codetype Product =
    { Id: int
      Name: string
      Price: decimal }
```

*You can then create a repository for the* `Product` *entity using the* `IRepository` *interface:*

```plaintext
codetype IProductRepository =
    abstract member GetById: int -> Async<Product option>
    abstract member GetAll: Async<seq<Product>>
    abstract member Add: Product -> Async<unit>
    abstract member Update: Product -> Async<unit>
    abstract member Remove: int -> Async<unit>
```

*To implement the repository, you will need to use Entity Framework Core. Here's an example of how you can do this using a context class and a* `Product` *entity:*

```plaintext
codetype ProductContext() =
    inherit DbContext()

    let productTable = Set<Product>()
    member x.Products with get() = productTable

type ProductRepository(context: ProductContext) =
    interface IProductRepository with
        member x.GetById id =
            async { return context.Products.SingleOrDefault(fun p -> p.Id = id) }
        member x.GetAll() =
            async { return context.Products.ToList() }
        member x.Add p =
            async {
                context.Products.Add(p)
                context.SaveChanges()
            }
        member x.Update p =
            async {
                let entity = context.Products.SingleOrDefault(fun e -> e.Id = p.Id)
                if entity <> null then
                    entity.Name <- p.Name
                    entity.Price <- p.Price
                    context.SaveChanges()
            }
        member x.Remove id =
            async {
                let entity = context.Products.SingleOrDefault(fun e -> e.Id = id)
                if entity <> null then
                    context.Products.Remove(entity)
                    context.SaveChanges()
            }
```

*Finally, you will need to configure Entity Framework to use your SQL Server database. You can do this by adding a connection string to your* `appsettings.json` *file:*

```plaintext
code{
  "ConnectionStrings": {
    "ProductDb": "Server=localhost;Database=ProductDb;Trusted_Connection=True;"
  }
}
```

*You can then use the* `ProductContext` *and* `ProductRepository` *classes in your application to perform CRUD operations on the* `Product` *entity.*

*I hope this helps! Let me know if you have any questions or if you need further assistance.*

![Thomas Cherickal](https://chat.openai.com/_next/image?url=https%3A%2F%2Flh3.googleusercontent.com%2Fa%2FAEdFTp7h6Hw9EN3Tk8o1UgJ_F80KYEkIppfFa9TYWevEnA%3Ds96-c&w=64&q=75 align="left")

**I want the same thing in multiple files**

*Sure! Here's an example of how you can split the code into multiple files:*

`Product.fs`*:*

```plaintext
codetype Product =
    { Id: int
      Name: string
      Price: decimal }
```

`ProductRepository.fs`*:*

```plaintext
codetype IProductRepository =
    abstract member GetById: int -> Async<Product option>
    abstract member GetAll: Async<seq<Product>>
    abstract member Add: Product -> Async<unit>
    abstract member Update: Product -> Async<unit>
    abstract member Remove: int -> Async<unit>

type ProductContext() =
    inherit DbContext()

    let productTable = Set<Product>()
    member x.Products with get() = productTable

type ProductRepository(context: ProductContext) =
    interface IProductRepository with
        member x.GetById id =
            async { return context.Products.SingleOrDefault(fun p -> p.Id = id) }
        member x.GetAll() =
            async { return context.Products.ToList() }
        member x.Add p =
            async {
                context.Products.Add(p)
                context.SaveChanges()
            }
        member x.Update p =
            async {
                let entity = context.Products.SingleOrDefault(fun e -> e.Id = p.Id)
                if entity <> null then
                    entity.Name <- p.Name
                    entity.Price <- p.Price
                    context.SaveChanges()
            }
        member x.Remove id =
            async {
                let entity = context.Products.SingleOrDefault(fun e -> e.Id = id)
                if entity <> null then
                    context.Products.Remove(entity)
                    context.SaveChanges()
            }
```

`appsettings.json`*:*

```plaintext
code{
  "ConnectionStrings": {
    "ProductDb": "Server=localhost;Database=ProductDb;Trusted_Connection=True;"
  }
}
```

*You can then use the* `ProductContext` *and* `ProductRepository` *classes in your application to perform CRUD operations on the* `Product` *entity.*

*I hope this helps! Let me know if you have any questions or if you need further assistance.*

### My God - What Have We Done!

(First recorded quote after the atom bomb in Hiroshima In WW2)

Coming Up:

[Part 3 - Convolutional Neural Networks](https://hashnode.com/edit/clcdsf26f000308i3cmud21mh)