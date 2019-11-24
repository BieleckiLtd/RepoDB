
[![Build status](https://img.shields.io/appveyor/ci/mikependon/repodb-h87g9?label=solution%20builds&style=for-the-badge)](https://ci.appveyor.com/project/mikependon/repodb-h87g9)
[![Build status](https://img.shields.io/nuget/dt/repodb?label=core%20dl%28s%29&style=for-the-badge)](https://www.nuget.org/packages/RepoDb)
[![Build status](https://img.shields.io/nuget/dt/repodb.sqlite?label=sqlite%20dl%28s%29&style=for-the-badge)](https://www.nuget.org/packages/RepoDb.SqLite)
[![Build status](https://img.shields.io/nuget/dt/repodb.mysql?label=mysql%20dl%28s%29&style=for-the-badge)](https://www.nuget.org/packages/RepoDb.MySql)

<img src="https://raw.githubusercontent.com/mikependon/RepoDb/master/RepoDb.Icons/RepoDb-64x64.png" height="64px" />

## RepoDb - a hybrid ORM library for .NET.

RepoDb provides the feature of micro and full ORMs. It help the developers to simplify the �switchover� of when to use the �micro� and �full� operations during the development.

**It is high-performance**

The word �high-performance� refers to �how fast� this ORM converts the raw data into a class object, and transport the class object as an actual data in the database.

RepoDb has its owns compiler. It caches the �already-generated� ILs and Expressions and reusing them for the upcoming transformations. Furthermore, RepoDb caches the �already-executed� operation context and reusing it for future calls.

**It is efficient**

The word �efficient� refers to �how well-managed� this ORM uses the computer memory when manipulating the objects all throughout the cycle of the operations.

RepoDb caches the �already-extracted� object properties and reusing it all throughout the process of transformations and executions. It helps eliminate the creation of unnecessary class objects.

## Highlights

 - RepoDb is the fastest and the most efficient ORM library in .NET as per the result of [RawDataAccessBencher](https://github.com/FransBouma/RawDataAccessBencher). See the actual execution results [here](https://github.com/FransBouma/RawDataAccessBencher/blob/master/Results/20190520_netcore.txt).
 - RepoDb is covered by thousand of major Unit Tests and Integration Tests.
 - RepoDb is running various critical applications in Production Environment.

## Builds

Project/Solution               | Status                                                                                                                                                   | Test Results                                                                                                                                                            |
-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
RepoDb.Core                    | [![Build status](https://img.shields.io/appveyor/ci/mikependon/repodb-ek0nw?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-ek0nw) | [![Build status](https://img.shields.io/appveyor/tests/mikependon/repodb-ek0nw?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-ek0nw/build/tests) |
RepoDb.Core.UnitTests	       | [![Build status](https://img.shields.io/appveyor/ci/mikependon/repodb-yf1cx?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-yf1cx) | [![Build status](https://img.shields.io/appveyor/tests/mikependon/repodb-yf1cx?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-yf1cx/build/tests) |
RepoDb.Core.IntegrationTests   | [![Build status](https://img.shields.io/appveyor/ci/mikependon/repodb-qksas?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-qksas) | [![Build status](https://img.shields.io/appveyor/tests/mikependon/repodb-qksas?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-qksas/build/tests) |
RepoDb.SqLite                  | [![Build status](https://img.shields.io/appveyor/ci/mikependon/repodb-o6787?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-o6787) | [![Build status](https://img.shields.io/appveyor/tests/mikependon/repodb-o6787?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-o6787/build/tests) |
RepoDb.SqLite.UnitTests        | [![Build status](https://img.shields.io/appveyor/ci/mikependon/repodb-mhpo4?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-mhpo4) | [![Build status](https://img.shields.io/appveyor/tests/mikependon/repodb-mhpo4?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-mhpo4/build/tests) |
RepoDb.SqLite.IntegrationTests | [![Build status](https://img.shields.io/appveyor/ci/mikependon/repodb-eg27p?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-eg27p) | [![Build status](https://img.shields.io/appveyor/tests/mikependon/repodb-eg27p?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-eg27p/build/tests) |
RepoDb.MySql                   | [![Build status](https://img.shields.io/appveyor/ci/mikependon/repodb-6adn4?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-6adn4) | [![Build status](https://img.shields.io/appveyor/tests/mikependon/repodb-6adn4?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-6adn4/build/tests) |
RepoDb.MySql.UnitTests         | [![Build status](https://img.shields.io/appveyor/ci/mikependon/repodb-t2hy7?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-t2hy7) | [![Build status](https://img.shields.io/appveyor/tests/mikependon/repodb-t2hy7?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-t2hy7/build/tests) |
RepoDb.MySql.IntegrationTests  | [![Build status](https://img.shields.io/appveyor/ci/mikependon/repodb-o4t48?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-o4t48) | [![Build status](https://img.shields.io/appveyor/tests/mikependon/repodb-o4t48?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-o4t48/build/tests) |

## Supported Databases

Practically, RepoDb has supported all RDBMS data-providers. Developers has the freedom to write their own SQL statement and execute it against the database in one-go. The execution of the SQL statements limit only from the �Execute� methods the RepoDb has provided (ie: *ExecuteQuery*, *ExecuteNonQuery*, *ExecuteScalar*, *ExecuteReader* and *ExecuteQueryMultiple*).

**Full support via Fluent-Methods**

<img src="https://github.com/mikependon/RepoDb/blob/master/RepoDb.Wiki/Images/SqlServer.png?raw=true" height="96px" title="SqlServer" /> <img src="https://raw.githubusercontent.com/mikependon/RepoDb/master/RepoDb.Wiki/Images/SQLite.png" height="96px" title="SqLite" /> <img src="https://raw.githubusercontent.com/mikependon/RepoDb/master/RepoDb.Wiki/Images/MySql.png" height="96px" title="MySql" /> <img src="https://raw.githubusercontent.com/mikependon/RepoDb/master/RepoDb.Wiki/Images/PostgreSql.png" height="96px" title="PostgreSql" />

RepoDb has provided the �Fluent� methods in which the SQL Statements are automatically being constructed as the operations are being executed. These methods are the most common operations being used by most developers. In this regards, RepoDb only fully supported the *SQL Server*, *SQLite*, *MySQL* and *PostgreSQL (soon)* data providers.

## Core Features
 
 - Asynchronous Operations
 - Batch Operations
 - Bulk Operations
 - Caching
 - Connection Persistency
 - Database Helpers
 - Database Settings
 - Expression Trees
 - Extension Methods
 - Field Mapping
 - Inline Hints
 - Massive Operations (Generics/Explicits/MethodCalls/TableBased)
 - Multi-Resultset Query
 - Query Builder
 - Repositories
 - Resolvers (CLR Types, DB Types)
 - Statement Builder
 - Tracing
 - Transaction
 - Type Mapping

## Examples

Let us say you have a customer class named `Customer` that has an equivalent table in the database named `[dbo].[Customer]`.

```csharp
public class Customer
{
	public int Id { get; set; }
	public string FirstName { get; set; }
	public string LastName { get; set; }
	public bool IsActive { get; set; }
	public DateTime LastUpdatedUtc { get; set; }
	public DateTime CreatedDateUtc { get; set; }
}
```

### Query<TEntity>

Via PrimaryKey:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query<Customer>(10045);
}
```

Via Dynamic:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query<Customer>(new { Id = 10045 });
}
```

Via Expression:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query<Customer>(c => c.Id == 10045);
}
```

Via Object:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query<Customer>(new QueryField(nameof(Customer.Id), 10045));
}
```

### Query(TableName)

Via PrimaryKey:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query("Customer", 10045);
}
```

Via Dynamic:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query("Customer", new { Id = 10045 });
}
```

Via Object:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query("Customer", new QueryField(nameof(Customer.Id), 10045));
}
```
	
Via Object (targetting few fields):

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query("Customer", new QueryField(nameof(Customer.Id), 10045),
		Field.From("Id", "FirstName", "LastName"));
}
```

### Insert<TEntity>

```csharp
var customer = new Customer
{
	FirstName = "John",
	LastName = "Doe",
	IsActive = true
};
using (var connection = new SqlConnection(ConnectionString))
{
	var id = connection.Insert<Customer, int>(customer);
}
```

### Insert(TableName)

```csharp
var customer = new
{
	FirstName = "John",
	LastName = "Doe",
	IsActive = true,
	LastUpdatedUtc = DateTime.Utc,
	CreatedDateUtc = DateTime.Utc
};
using (var connection = new SqlConnection(ConnectionString))
{
	var id = connection.Insert<int>("Customer", customer);
}
```

### Update<TEntity>

Via DataEntity:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query<Customer>(10045);
	customer.FirstName = "John";
	customer.LastUpdatedUtc = DateTime.UtcNow;
	var affectedRows = connection.Update<Customer>(customer);
}
```

Via PrimaryKey:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query<Customer>(10045);
	customer.FirstName = "John";
	customer.LastUpdatedUtc = DateTime.UtcNow;
	var affectedRows = connection.Update<Customer>(customer, 10045);
}
```

Via Dynamic:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query<Customer>(10045);
	customer.FirstName = "John";
	customer.LastUpdatedUtc = DateTime.UtcNow;
	var affectedRows = connection.Update<Customer>(customer, new { Id = 10045 });
}
```

Via Expression:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query<Customer>(10045);
	customer.FirstName = "John";
	customer.LastUpdatedUtc = DateTime.UtcNow;
	var affectedRows = connection.Update<Customer>(customer, e => e.Id == 10045);
}
```
	
Via Object:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query<Customer>(10045);
	customer.FirstName = "John";
	customer.LastUpdatedUtc = DateTime.UtcNow;
	var affectedRows = connection.Update<Customer>(customer, new QueryField(nameof(Customer.Id), 10045));
}
```

### Update(TableName)

Via Dynamic Object:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = new
	{
		Id = 10045,
		FirstName = "John",
		LastUpdatedUtc = DateTime.UtcNow
	};
	var affectedRows = connection.Update("Customer", customer);
}
```

Via PrimaryKey:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = new
	{
		FirstName = "John",
		LastUpdatedUtc = DateTime.UtcNow
	};
	var affectedRows = connection.Update("Customer", customer, 10045);
}
```

Via Dynamic:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = new
	{
		FirstName = "John",
		LastUpdatedUtc = DateTime.UtcNow
	};
	var affectedRows = connection.Update("Customer", customer, new { Id = 10045 });
}
```
	
Via Object:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = new
	{
		FirstName = "John",
		LastUpdatedUtc = DateTime.UtcNow
	};
	var affectedRows = connection.Update("Customer", customer, new QueryField("Id", 10045));
}
```

### Delete<TEntity>

Via DataEntity:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query<Customer>(10045);
	var deletedCount = connection.Delete<Customer>(customer);
}
```

Via PrimaryKey:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var deletedCount = connection.Delete<Customer>(10045);
}
```

Via Dynamic:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var deletedCount = connection.Delete<Customer>(new { Id = 10045 });
}
```

Via Expression:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var deletedCount = connection.Delete<Customer>(c => c.Id == 10045);
}
```

Via Object:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var deletedCount = connection.Delete<Customer>(new QueryField(nameof(Customer.Id), 10045));
}
```

### Delete(TableName)

Via PrimaryKey:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var deletedCount = connection.Delete("Customer", 10045);
}
```

Via Dynamic:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var deletedCount = connection.Delete("Customer", { Id = 10045 });
}
```

Via Object:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var deletedCount = connection.Delete("Customer", new QueryField(nameof(Customer.Id), 10045));
}
```

### Merge<TEntity>

```csharp
var customer = new Customer
{
	FirstName = "John",
	LastName = "Doe",
	IsActive = true,
	LastUpdatedUtc = DateTime.Utc,
	CreatedDateUtc = DateTime.Utc
};
using (var connection = new SqlConnection(ConnectionString))
{
	var qualifiers = new []
	{
		new Field(nameof(Customer.FirstName)),
		new Field(nameof(Customer.LastName)),
	};
	var mergeCount = connection.Merge<Customer>(customer, qualifiers);
}
```

### Merge(TableName)

```csharp
var customer = new Customer
{
	FirstName = "John",
	LastName = "Doe",
	IsActive = true
};
using (var connection = new SqlConnection(ConnectionString))
{
	var qualifiers = new []
	{
		new Field(nameof(Customer.FirstName)),
		new Field(nameof(Customer.LastName)),
	};
	var mergeCount = connection.Merge("Customer", customer, qualifiers);
}
```

### ExecuteQuery

You can create a class with combined properties of different tables or with stored procedures. It does not need to be 100% identical to the schema, as long the property of the class is part of the result set.

```csharp
public class ComplexClass
{
	public int CustomerId { get; set; }
	public int OrderId { get; set; }
	public int ProductId { get; set; }
	public string CustomerName { get; set; }
	public string ProductName { get; set; }
	public DateTime ProductDescription { get; set; } // This is not in the CommandText, will be ignored
	public DateTime OrderDate { get; set; }
	public int Quantity { get; set; }
	public double Price { get; set; }
}
```

Then you can create this command text.

	var commandText = @"SELECT C.Id AS CustomerId
		, O.Id AS OrderId
		, P.Id AS ProductId
		, CONCAT(C.FirstName, ' ', C.LastName) AS CustomerName
		, P.Name AS ProductName
		, O.OrderDate
		, O.Quantity
		, P.Price
		, (O.Quatity * P.Price) AS Total /* Note: This is not in the class, but still it is valid */
	FROM [dbo].[Customer] C
	INNER JOIN [dbo].[Order] O ON O.CustomerId = C.Id
	INNER JOIN [dbo].[OrderItem] OI ON OI.OrderId = O.Id
	INNER JOIN [dbo].[Product] P ON P.Id = OI.ProductId
	WHERE (C.Id = @CustomerId)
		AND (O.OrderDate BETWEEN @OrderDate AND DATEADD(DAY, 1, @OrderDate));";

Via Dynamic:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.ExecuteQuery<ComplexClass>(commandText, new { CustomerId = 10045, OrderDate = DateTime.UtcNow.Date });
}
```

Via Object:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var queryGroup = new QueryGroup(new []
	{
		new QueryField("CustomerId", 10045),
		new QueryField("OrderDate", DateTime.UtcNow.Date)
	});
	var customer = connection.ExecuteQuery<Customer>(commandText, queryGroup);
}
```

The `ExecuteQuery` method is purposely not being supported by `Expression` based query as we are avoiding the user to bind the complex-class to its target query text.

Note: The most optimal when it comes to performance is to used the `Object-Based`.

### StoredProcedure

Using the complex type above. If you have a stored procedure like below.

	DROP PROCEDURE IF EXISTS [dbo].[sp_get_customer_orders_by_date];
	GO
	CREATE PROCEDURE [dbo].[sp_get_customer_orders_by_date]
	(
		@CustomerId INT
		, @OrderDate DATETIME2(7)
	)
	AS
	BEGIN
		SELECT C.Id AS CustomerId
			, O.Id AS OrderId
			, P.Id AS ProductId
			, CONCAT(C.FirstName, ' ', C.LastName) AS CustomerName
			, P.Name AS ProductName
			, O.OrderDate
			, O.Quantity
			, P.Price
			, (O.Quatity * P.Price) AS Total /* Note: This is not in the class, but still it is valid */
		FROM [dbo].[Customer] C
		INNER JOIN [dbo].[Order] O ON O.CustomerId = C.Id
		INNER JOIN [dbo].[OrderItem] OI ON OI.OrderId = O.Id
		INNER JOIN [dbo].[Product] P ON P.Id = OI.ProductId
		WHERE (C.Id = @CustomerId)
			AND (O.OrderDate BETWEEN @OrderDate AND DATEADD(DAY, 1, @OrderDate));
	END

Then it can be called as below.

Via Dynamic:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.ExecuteQuery<ComplexClass>("[dbo].[sp_get_customer_orders_by_date]",
		param: new { CustomerId = 10045, OrderDate = DateTime.UtcNow.Date },
		commandType: CommandType.StoredProcedure);
}
```

Via Object:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var queryGroup = new QueryGroup(new []
	{
		new QueryField("CustomerId", 10045),
		new QueryField("OrderDate", DateTime.UtcNow.Date)
	});
	var customer = connection.ExecuteQuery<Customer>(commandText, queryGroup,
		commandType: CommandType.StoredProcedure);
}
```

Please visit our [documentation](https://repodb.readthedocs.io/en/latest/) for further details about the codes.
