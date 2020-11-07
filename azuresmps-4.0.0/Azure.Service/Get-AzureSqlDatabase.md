---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 7427A101-9439-45B9-B72E-F8C2DA85E412
online version: ''
schema: 2.0.0
ms.openlocfilehash: c10ae808d105079b9739516bf9eaf316241b1b11
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946298"
---
# <span data-ttu-id="e6f4a-101">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e6f4a-101">Get-AzureSqlDatabase</span></span>

## <span data-ttu-id="e6f4a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6f4a-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f4a-103">Recupera um ou mais bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-103">Retrieves one or more databases.</span></span>

## <span data-ttu-id="e6f4a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6f4a-104">SYNTAX</span></span>

### <span data-ttu-id="e6f4a-105">ByConnectionContext (padrão)</span><span class="sxs-lookup"><span data-stu-id="e6f4a-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-RestorableDropped] [-RestorableDroppedDatabase <RestorableDroppedDatabase>]
 [-DatabaseDeletionDate <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e6f4a-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="e6f4a-106">ByServerName</span></span>
```
Get-AzureSqlDatabase -ServerName <String> [-Database <Database>] [-DatabaseName <String>] [-RestorableDropped]
 [-RestorableDroppedDatabase <RestorableDroppedDatabase>] [-DatabaseDeletionDate <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e6f4a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e6f4a-107">DESCRIPTION</span></span>
<span data-ttu-id="e6f4a-108">O cmdlet **Get-AzureSqlDatabase** recupera uma ou mais instâncias de um banco de dados SQL do Azure de um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-108">The **Get-AzureSqlDatabase** cmdlet retrieves one or more instances of an Azure SQL Database from an Azure SQL Database server.</span></span>
<span data-ttu-id="e6f4a-109">Você pode especificar o servidor com um contexto de conexão de servidor de banco de dados SQL do Azure que você cria usando o cmdlet **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="e6f4a-109">You can specify the server with an Azure SQL Database server connection context that you create using the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="e6f4a-110">Ou, se você especificar o nome do servidor do banco de dados SQL do Azure, o cmdlet usará as informações atuais da assinatura do Azure para autenticar a solicitação de acesso ao servidor.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-110">Or, if you specify the Azure SQL Database server name, the cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

<span data-ttu-id="e6f4a-111">Se você não especificar um banco de dados, o cmdlet **Get-AzureSqlDatabase** retornará todos os bancos de dados do servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-111">If you do not specify a database, the **Get-AzureSqlDatabase** cmdlet returns all databases from the specified server.</span></span>

<span data-ttu-id="e6f4a-112">Recuperando bancos de dados recuperáveis desconectados:</span><span class="sxs-lookup"><span data-stu-id="e6f4a-112">Retrieving restorable dropped databases:</span></span>

<span data-ttu-id="e6f4a-113">Recupere bancos de dados recuperáveis desconectados usando o parâmetro *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="e6f4a-113">Retrieve restorable dropped databases by using the *RestorableDropped* parameter.</span></span>
<span data-ttu-id="e6f4a-114">Para retornar todos os bancos de dados removidos recuperáveis, use o parâmetro *RestorableDropped* sem *DatabaseName* e *DatabaseDeletionDate*.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-114">To return all restorable dropped databases use the *RestorableDropped* parameter without *DatabaseName* and *DatabaseDeletionDate*.</span></span>
<span data-ttu-id="e6f4a-115">Para retornar um banco de dados recuperável específico, use o parâmetro *RestorableDropped* com os parâmetros *DatabaseName* e *DatabaseDeletionDate* .</span><span class="sxs-lookup"><span data-stu-id="e6f4a-115">To return a specific restorable dropped database use the *RestorableDropped* parameter with the *DatabaseName* and *DatabaseDeletionDate* parameters.</span></span>
<span data-ttu-id="e6f4a-116">Ao recuperar um banco de dados recuperável específico usando o parâmetro *DatabaseName* , você também deve incluir o parâmetro *DatabaseDeletionDate* e o valor *DatabaseDeletionDate* especificado deve incluir milissegundos para corresponder ao banco de dados desejado.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-116">When retrieving a specific restorable dropped database by using the *DatabaseName* parameter you must also include the *DatabaseDeletionDate* parameter and the specified *DatabaseDeletionDate* value must include milliseconds to match the desired database.</span></span>

<span data-ttu-id="e6f4a-117">O cmdlet **Get-AzureSqlDatabase** retorna todos os bancos de dados removidos recuperáveis em um servidor ou um banco de dados específico que corresponda a *DatabaseName* e *DatabaseDeletionDate*.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-117">The **Get-AzureSqlDatabase** cmdlet returns either all restorable dropped databases on a server, or one specific database that matches both *DatabaseName* and *DatabaseDeletionDate*.</span></span>
<span data-ttu-id="e6f4a-118">Para retornar os bancos de dados removidos recuperáveis que satisfaçam critérios diferentes, como todos os bancos de dados removidos recuperáveis de um nome específico, você deve retornar todos os bancos de dados recuperáveis e filtrar os resultados no cliente.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-118">To return restorable dropped databases that satisfy different criteria, such as all restorable dropped databases of a specific name, you must return all restorable dropped databases, and then filter the results on the client.</span></span>

## <span data-ttu-id="e6f4a-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e6f4a-119">EXAMPLES</span></span>

### <span data-ttu-id="e6f4a-120">Exemplo 1: recuperar todos os bancos de dados em um servidor</span><span class="sxs-lookup"><span data-stu-id="e6f4a-120">Example 1: Retrieve all databases on a server</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="e6f4a-121">Esse comando recupera todos os bancos de dados no servidor chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-121">This command retrieves all databases on the server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="e6f4a-122">Exemplo 2: recuperar todos os bancos de dados removidos recuperáveis em um servidor</span><span class="sxs-lookup"><span data-stu-id="e6f4a-122">Example 2: Retrieve all restorable dropped databases on a server</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped
```

<span data-ttu-id="e6f4a-123">Esse comando recupera todos os bancos de dados removidos recuperáveis no servidor chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-123">This command retrieves all restorable dropped databases on the server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="e6f4a-124">Exemplo 3: recuperar um banco de dados de um servidor especificado por um contexto de conexão</span><span class="sxs-lookup"><span data-stu-id="e6f4a-124">Example 3: Retrieve a database from a server specified by a connection context</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

<span data-ttu-id="e6f4a-125">Esse comando recupera o banco de dados denominado Database01 do servidor especificado pelo contexto de conexão $Context.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-125">This command retrieves database named Database01 from the server specified by the connection context $Context.</span></span>

### <span data-ttu-id="e6f4a-126">Exemplo 4: armazenar um objeto de banco de dados em uma variável</span><span class="sxs-lookup"><span data-stu-id="e6f4a-126">Example 4: Store a database object in a variable</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

<span data-ttu-id="e6f4a-127">Esse comando recupera o banco de dados denominado Database01 do servidor chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-127">This command retrieves database named Database01 from the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="e6f4a-128">O comando armazena o objeto de banco de dados na variável $Database 01.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-128">The command stores the database object in the $Database01 variable.</span></span>

### <span data-ttu-id="e6f4a-129">Exemplo 5: recuperar um banco de dados recuperável removido</span><span class="sxs-lookup"><span data-stu-id="e6f4a-129">Example 5: Retrieve a restorable dropped database</span></span>
```
PS C:\> $DroppedDB = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" -RestorableDropped
```

<span data-ttu-id="e6f4a-130">Esse comando recupera o banco de dados removido recuperável chamado Database01 que foi excluído no 11/9/2012 do servidor chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-130">This command retrieves the restorable dropped database named Database01 that was deleted on 11/9/2012 from the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="e6f4a-131">Esse comando armazena os resultados na variável $DroppedDB.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-131">This command stores the results in the $DroppedDB variable.</span></span>

### <span data-ttu-id="e6f4a-132">Exemplo 6: recuperar todos os bancos de dados removidos recuperáveis em um servidor e filtrar os resultados</span><span class="sxs-lookup"><span data-stu-id="e6f4a-132">Example 6: Retrieve all restorable dropped databases on a server and filter the results</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped | Where-Object {$_.Name -eq "ContactDB"}
```

<span data-ttu-id="e6f4a-133">Esse comando recupera todos os bancos de dados removidos recuperáveis no servidor chamado lpqd0zbr8y e filtra os resultados somente para bancos de dados chamados ContactDB.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-133">This command retrieves all restorable dropped databases on the server named lpqd0zbr8y, and then filters the results to only the databases named ContactDB.</span></span>

## <span data-ttu-id="e6f4a-134">OS</span><span class="sxs-lookup"><span data-stu-id="e6f4a-134">PARAMETERS</span></span>

### <span data-ttu-id="e6f4a-135">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="e6f4a-135">-ConnectionContext</span></span>
<span data-ttu-id="e6f4a-136">Especifica o contexto de conexão de um servidor do qual recuperar um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-136">Specifies the connection context of a server from which to retrieve a database.</span></span>

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

### <span data-ttu-id="e6f4a-137">-Banco de dados</span><span class="sxs-lookup"><span data-stu-id="e6f4a-137">-Database</span></span>
<span data-ttu-id="e6f4a-138">Especifica um objeto que representa o banco de dados recuperado pelo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-138">Specifies an object that represents the database that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="e6f4a-139">-DatabaseDeletionDate</span><span class="sxs-lookup"><span data-stu-id="e6f4a-139">-DatabaseDeletionDate</span></span>
<span data-ttu-id="e6f4a-140">Especifica a data e a hora de uma exclusão.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-140">Specifies the date and time of a deletion.</span></span>
<span data-ttu-id="e6f4a-141">Se você especificar o parâmetro *RestorableDropped* , especifique esse parâmetro para recuperar um banco de dados recuperável Descartado com base na data e hora de exclusão.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-141">If you specify the *RestorableDropped* parameter, specify this parameter to retrieve a restorable dropped database based on the deletion date and time.</span></span>

<span data-ttu-id="e6f4a-142">O parâmetro *DatabaseDeletionDate* deve incluir milissegundos para corresponder ao tempo do banco de dados desejado.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-142">The *DatabaseDeletionDate* parameter must include milliseconds to match the time of the desired database.</span></span>
<span data-ttu-id="e6f4a-143">Especificar um valor sem nenhum resultado de milissegundos não é possível localizar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-143">Specifying a value without milliseconds results in the database not being found.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f4a-144">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e6f4a-144">-DatabaseName</span></span>
<span data-ttu-id="e6f4a-145">Especifica o nome do banco de dados que este cmdlet recupera.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-145">Specifies the name of the database that this cmdlet retrieves.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f4a-146">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e6f4a-146">-Profile</span></span>
<span data-ttu-id="e6f4a-147">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e6f4a-148">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e6f4a-149">-RestorableDropped</span><span class="sxs-lookup"><span data-stu-id="e6f4a-149">-RestorableDropped</span></span>
<span data-ttu-id="e6f4a-150">Indica que esse cmdlet retorna objetos *RestorableDroppedDatabase* em vez de objetos de *banco de dados* .</span><span class="sxs-lookup"><span data-stu-id="e6f4a-150">Indicates that this cmdlet returns *RestorableDroppedDatabase* objects instead of *Database* objects.</span></span>
<span data-ttu-id="e6f4a-151">Você pode usar o parâmetro *DatabaseDeletionDate* para selecionar um banco de dados recuperável que pode ser removida.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-151">You can use the *DatabaseDeletionDate* parameter to select a specific restorable dropped database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f4a-152">-RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="e6f4a-152">-RestorableDroppedDatabase</span></span>
<span data-ttu-id="e6f4a-153">Especifica um objeto que representa o banco de dados recuperável ignorado que esse cmdlet recupera.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-153">Specifies an object that represents the restorable dropped database that this cmdlet retrieves.</span></span>

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6f4a-154">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="e6f4a-154">-ServerName</span></span>
<span data-ttu-id="e6f4a-155">Especifica o nome do servidor que contém o banco de dados que este cmdlet recupera.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-155">Specifies the name of the server that contains the database that this cmdlet retrieves.</span></span>
<span data-ttu-id="e6f4a-156">O cmdlet usa a assinatura atual do Azure para acessar o servidor.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-156">The cmdlet uses the current Azure subscription to access the server.</span></span>

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

### <span data-ttu-id="e6f4a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f4a-157">CommonParameters</span></span>
<span data-ttu-id="e6f4a-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6f4a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f4a-159">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6f4a-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f4a-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e6f4a-160">INPUTS</span></span>

### <span data-ttu-id="e6f4a-161">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="e6f4a-161">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

### <span data-ttu-id="e6f4a-162">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="e6f4a-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase</span></span>

## <span data-ttu-id="e6f4a-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e6f4a-163">OUTPUTS</span></span>

### <span data-ttu-id="e6f4a-164">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\></span><span class="sxs-lookup"><span data-stu-id="e6f4a-164">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\></span></span>
<span data-ttu-id="e6f4a-165">Esse cmdlet retorna um objeto de *banco de dados* se você não especificar o parâmetro *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="e6f4a-165">This cmdlet returns a *Database* object if you do not specify the *RestorableDropped* parameter.</span></span>

### <span data-ttu-id="e6f4a-166">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\></span><span class="sxs-lookup"><span data-stu-id="e6f4a-166">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\></span></span>
<span data-ttu-id="e6f4a-167">Esse cmdlet retorna um objeto *RestorableDroppedDatabase* se você especificar o parâmetro *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="e6f4a-167">This cmdlet returns a *RestorableDroppedDatabase* object if you specify the *RestorableDropped* parameter.</span></span>

## <span data-ttu-id="e6f4a-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e6f4a-168">NOTES</span></span>

## <span data-ttu-id="e6f4a-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6f4a-169">RELATED LINKS</span></span>

[<span data-ttu-id="e6f4a-170">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="e6f4a-170">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="e6f4a-171">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="e6f4a-171">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="e6f4a-172">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e6f4a-172">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="e6f4a-173">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="e6f4a-173">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="e6f4a-174">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e6f4a-174">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="e6f4a-175">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e6f4a-175">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


