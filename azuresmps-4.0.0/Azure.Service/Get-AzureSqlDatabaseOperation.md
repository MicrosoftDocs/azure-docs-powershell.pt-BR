---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 56026A74-A6DC-47A5-9643-5828C3D0E83B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32219154f2036ee028b05a369c46be1d8e1def87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946293"
---
# <span data-ttu-id="81a8e-101">Get-AzureSqlDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="81a8e-101">Get-AzureSqlDatabaseOperation</span></span>

## <span data-ttu-id="81a8e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81a8e-102">SYNOPSIS</span></span>
<span data-ttu-id="81a8e-103">Obtém o status das operações de banco de dados em um servidor do Azure.</span><span class="sxs-lookup"><span data-stu-id="81a8e-103">Gets the status of database operations on an Azure server.</span></span>

## <span data-ttu-id="81a8e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81a8e-104">SYNTAX</span></span>

### <span data-ttu-id="81a8e-105">ByConnectionContext (padrão)</span><span class="sxs-lookup"><span data-stu-id="81a8e-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabaseOperation -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="81a8e-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="81a8e-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseOperation -ServerName <String> [-Database <Database>] [-DatabaseName <String>]
 [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="81a8e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81a8e-107">DESCRIPTION</span></span>
<span data-ttu-id="81a8e-108">O cmdlet **Get-AzureSqlDatabaseOperation** Obtém o status das operações de banco de dados no servidor do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="81a8e-108">The **Get-AzureSqlDatabaseOperation** cmdlet gets the status of database operations on the specified Azure server.</span></span>
<span data-ttu-id="81a8e-109">Se você especificar somente o parâmetro *ServerName* ou *ConnectionContext* , o cmdlet obterá todas as operações de banco de dados para o servidor.</span><span class="sxs-lookup"><span data-stu-id="81a8e-109">If you specify only the *ServerName* or *ConnectionContext* parameter, the cmdlet gets all the database operations for the server.</span></span>
<span data-ttu-id="81a8e-110">Se você também especificar um banco de dados usando o parâmetro *Database* ou *DatabaseName* , esse cmdlet obterá todas as operações para o banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="81a8e-110">If you also specify a database by using the *Database* or *DatabaseName* parameter, this cmdlet gets all the operations for the specified database.</span></span>
<span data-ttu-id="81a8e-111">Se você especificar um GUID de operação e *nomedoservidor* ou *ConnectionContext* , o cmdlet receberá uma única operação de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="81a8e-111">If you specify an operation GUID, and *ServerName* or *ConnectionContext* , the cmdlet gets a single database operation.</span></span>

## <span data-ttu-id="81a8e-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81a8e-112">EXAMPLES</span></span>

### <span data-ttu-id="81a8e-113">Exemplo 1: obter o status de todas as operações de banco de dados de um banco de dados</span><span class="sxs-lookup"><span data-stu-id="81a8e-113">Example 1: Get the status of all database operations for a database</span></span>
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context -DatabaseName "Database17"
```

<span data-ttu-id="81a8e-114">Esse comando obtém o status de todas as operações de banco de dados no banco de dados chamada Database17 no servidor que o contexto de conexão $Context especifica.</span><span class="sxs-lookup"><span data-stu-id="81a8e-114">This command gets the status of all database operations on the database named Database17 on the server that the connection context $Context specifies.</span></span>

### <span data-ttu-id="81a8e-115">Exemplo 2: obter o status de todas as operações de banco de dados de um servidor</span><span class="sxs-lookup"><span data-stu-id="81a8e-115">Example 2: Get the status of all database operations for a server</span></span>
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context
```

<span data-ttu-id="81a8e-116">Esse comando obtém o status de todas as operações de banco de dados no servidor que o contexto de conexão $Context especifica.</span><span class="sxs-lookup"><span data-stu-id="81a8e-116">This command gets the status of all database operations on the server that the connection context $Context specifies.</span></span>

## <span data-ttu-id="81a8e-117">OS</span><span class="sxs-lookup"><span data-stu-id="81a8e-117">PARAMETERS</span></span>

### <span data-ttu-id="81a8e-118">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="81a8e-118">-ConnectionContext</span></span>
<span data-ttu-id="81a8e-119">Especifica o contexto de conexão de um servidor.</span><span class="sxs-lookup"><span data-stu-id="81a8e-119">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81a8e-120">-Banco de dados</span><span class="sxs-lookup"><span data-stu-id="81a8e-120">-Database</span></span>
<span data-ttu-id="81a8e-121">Especifica um objeto que representa um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="81a8e-121">Specifies an object that represents an Azure SQL Database.</span></span>
<span data-ttu-id="81a8e-122">Se você especificar esse parâmetro, deverá especificar o parâmetro *ServerName* ou o parâmetro *ConnectionContext* .</span><span class="sxs-lookup"><span data-stu-id="81a8e-122">If you specify this parameter, you must specify the *ServerName* parameter or *ConnectionContext* parameter.</span></span>

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81a8e-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="81a8e-123">-DatabaseName</span></span>
<span data-ttu-id="81a8e-124">Especifica o nome de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="81a8e-124">Specifies the name of a database.</span></span>
<span data-ttu-id="81a8e-125">Se você especificar esse parâmetro, deverá especificar o parâmetro *ServerName* ou o parâmetro *ConnectionContext* .</span><span class="sxs-lookup"><span data-stu-id="81a8e-125">If you specify this parameter, you must specify the *ServerName* parameter or the *ConnectionContext* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81a8e-126">-OperationGuid</span><span class="sxs-lookup"><span data-stu-id="81a8e-126">-OperationGuid</span></span>
<span data-ttu-id="81a8e-127">Especifica a ID da operação que representa uma operação de banco de dados específica para a qual esse cmdlet obtém o status.</span><span class="sxs-lookup"><span data-stu-id="81a8e-127">Specifies the operation ID that represents a specific database operation for which this cmdlet gets status.</span></span>
<span data-ttu-id="81a8e-128">Você pode obter IDs de operação solicitando todas as operações de banco de dados de um banco de dados SQL do Azure ou servidor.</span><span class="sxs-lookup"><span data-stu-id="81a8e-128">You can obtain operation IDs by requesting all the database operations for a Azure SQL Database or server.</span></span>
<span data-ttu-id="81a8e-129">Se você especificar esse parâmetro, deverá especificar o parâmetro *ServerName* ou o parâmetro *ConnectionContext* .</span><span class="sxs-lookup"><span data-stu-id="81a8e-129">If you specify this parameter, you must specify the *ServerName* parameter or the *ConnectionContext* parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81a8e-130">-Perfil</span><span class="sxs-lookup"><span data-stu-id="81a8e-130">-Profile</span></span>
<span data-ttu-id="81a8e-131">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="81a8e-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="81a8e-132">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="81a8e-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a8e-133">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="81a8e-133">-ServerName</span></span>
<span data-ttu-id="81a8e-134">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="81a8e-134">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81a8e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a8e-135">CommonParameters</span></span>
<span data-ttu-id="81a8e-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81a8e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a8e-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81a8e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a8e-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81a8e-138">INPUTS</span></span>

### <span data-ttu-id="81a8e-139">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="81a8e-139">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

### <span data-ttu-id="81a8e-140">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="81a8e-140">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

### <span data-ttu-id="81a8e-141">System. GUID</span><span class="sxs-lookup"><span data-stu-id="81a8e-141">System.Guid</span></span>

## <span data-ttu-id="81a8e-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81a8e-142">OUTPUTS</span></span>

### <span data-ttu-id="81a8e-143">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database. DatabaseOperationResponseList []</span><span class="sxs-lookup"><span data-stu-id="81a8e-143">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database.DatabaseOperationResponseList[]</span></span>
<span data-ttu-id="81a8e-144">Esse cmdlet retorna uma matriz de objetos **DatabaseOperationResponseList** se você obtém várias operações.</span><span class="sxs-lookup"><span data-stu-id="81a8e-144">This cmdlet returns an array of **DatabaseOperationResponseList** objects if you get multiple operations.</span></span>

### <span data-ttu-id="81a8e-145">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database. DatabaseOperationResponse</span><span class="sxs-lookup"><span data-stu-id="81a8e-145">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database.DatabaseOperationResponse</span></span>

## <span data-ttu-id="81a8e-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81a8e-146">NOTES</span></span>

## <span data-ttu-id="81a8e-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81a8e-147">RELATED LINKS</span></span>

[<span data-ttu-id="81a8e-148">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="81a8e-148">Azure SQL Database</span></span>](https://msdn.microsoft.com/library/ee336279.aspx)

[<span data-ttu-id="81a8e-149">Status da operação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="81a8e-149">Database Operation Status</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn720371.aspx)

[<span data-ttu-id="81a8e-150">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="81a8e-150">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="81a8e-151">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="81a8e-151">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="81a8e-152">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="81a8e-152">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


