---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F63769D6-9A31-4A67-972A-1E0428853C86
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88f61718e363a630b70519590025a6da80364aeb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945423"
---
# <span data-ttu-id="f137c-101">Start-AzureSqlDatabaseRecovery</span><span class="sxs-lookup"><span data-stu-id="f137c-101">Start-AzureSqlDatabaseRecovery</span></span>

## <span data-ttu-id="f137c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f137c-102">SYNOPSIS</span></span>
<span data-ttu-id="f137c-103">Inicia uma solicitação de restauração para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f137c-103">Initiates a restore request for a database.</span></span>

## <span data-ttu-id="f137c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f137c-104">SYNTAX</span></span>

### <span data-ttu-id="f137c-105">BySourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="f137c-105">BySourceDatabaseName</span></span>
```
Start-AzureSqlDatabaseRecovery -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f137c-106">BySourceDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="f137c-106">BySourceDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRecovery -SourceDatabase <RecoverableDatabase> [-TargetServerName <String>]
 [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f137c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f137c-107">DESCRIPTION</span></span>
<span data-ttu-id="f137c-108">O cmdlet **Start-AzureSqlDatabaseRecovery** inicia uma solicitação de restauração para um banco de dados ao vivo ou descartado.</span><span class="sxs-lookup"><span data-stu-id="f137c-108">The **Start-AzureSqlDatabaseRecovery** cmdlet initiates a restore request for a live or dropped database.</span></span>
<span data-ttu-id="f137c-109">Esse cmdlet dá suporte à recuperação básica que usa o último backup disponível conhecido para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f137c-109">This cmdlet supports basic recovery that uses the last known available backup for the database.</span></span>
<span data-ttu-id="f137c-110">A operação de recuperação cria um novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f137c-110">The recovery operation creates a new database.</span></span>
<span data-ttu-id="f137c-111">Se você recuperar um banco de dados dinâmico no mesmo servidor, você deve especificar um nome diferente para o novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f137c-111">If you recover a live database on the same server, you must specify a different name for the new database.</span></span>

<span data-ttu-id="f137c-112">Para fazer uma restauração point-in-time para um banco de dados, use o cmdlet **Start-AzureSqlDatabaseRestore** em vez disso.</span><span class="sxs-lookup"><span data-stu-id="f137c-112">To do a point in time restore for a database, use the **Start-AzureSqlDatabaseRestore** cmdlet instead.</span></span>

## <span data-ttu-id="f137c-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f137c-113">EXAMPLES</span></span>

### <span data-ttu-id="f137c-114">Exemplo 1: recuperar um banco de dados especificado como um objeto</span><span class="sxs-lookup"><span data-stu-id="f137c-114">Example 1: Recover a database specified as an object</span></span>
```
PS C:\> $Database = Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored"
```

<span data-ttu-id="f137c-115">O primeiro comando obtém um objeto de banco de dados usando o cmdlet **Get-AzureSqlRecoverableDatabase** .</span><span class="sxs-lookup"><span data-stu-id="f137c-115">The first command gets a database object by using the **Get-AzureSqlRecoverableDatabase** cmdlet.</span></span>
<span data-ttu-id="f137c-116">O comando armazena esse objeto na variável $Database.</span><span class="sxs-lookup"><span data-stu-id="f137c-116">The command stores that object in the $Database variable.</span></span>

<span data-ttu-id="f137c-117">O segundo comando recupera o banco de dados armazenado em $Database.</span><span class="sxs-lookup"><span data-stu-id="f137c-117">The second command recovers the database stored in $Database.</span></span>

### <span data-ttu-id="f137c-118">Exemplo 2: recuperar um banco de dados especificado pelo nome</span><span class="sxs-lookup"><span data-stu-id="f137c-118">Example 2: Recover a database specified by name</span></span>
```
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored"
```

<span data-ttu-id="f137c-119">Esse comando recupera um banco de dados usando o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f137c-119">This command recovers a database using the database name.</span></span>

## <span data-ttu-id="f137c-120">OS</span><span class="sxs-lookup"><span data-stu-id="f137c-120">PARAMETERS</span></span>

### <span data-ttu-id="f137c-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="f137c-121">-Profile</span></span>
<span data-ttu-id="f137c-122">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="f137c-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f137c-123">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="f137c-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f137c-124">-SourceDatabase</span><span class="sxs-lookup"><span data-stu-id="f137c-124">-SourceDatabase</span></span>
<span data-ttu-id="f137c-125">Especifica o objeto de banco de dados que representa o banco de dados que este cmdlet recupera.</span><span class="sxs-lookup"><span data-stu-id="f137c-125">Specifies the database object that represents the database that this cmdlet recovers.</span></span>

```yaml
Type: RecoverableDatabase
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f137c-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="f137c-126">-SourceDatabaseName</span></span>
<span data-ttu-id="f137c-127">Especifica o nome do banco de dados que este cmdlet recupera.</span><span class="sxs-lookup"><span data-stu-id="f137c-127">Specifies the name of the database that this cmdlet recovers.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f137c-128">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="f137c-128">-SourceServerName</span></span>
<span data-ttu-id="f137c-129">Especifica o nome do servidor no qual o banco de dados de origem está em tempo real ou em execução, ou no qual o banco de dados de origem foi executado antes de ser excluído.</span><span class="sxs-lookup"><span data-stu-id="f137c-129">Specifies the name of the server on which the source database is live and running, or on which the source database ran before it was deleted.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f137c-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="f137c-130">-TargetDatabaseName</span></span>
<span data-ttu-id="f137c-131">Especifica o nome do banco de dados recuperado.</span><span class="sxs-lookup"><span data-stu-id="f137c-131">Specifies the name of the recovered database.</span></span>
<span data-ttu-id="f137c-132">Se o banco de dados de origem ainda estiver ao vivo, para recuperá-lo para o mesmo servidor, você deve especificar um nome diferente do nome do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="f137c-132">If the source database is still live, in order to recover it to the same server, you must specify a name that differs from the source database name.</span></span>

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

### <span data-ttu-id="f137c-133">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="f137c-133">-TargetServerName</span></span>
<span data-ttu-id="f137c-134">Especifica o nome do servidor para o qual restaurar um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f137c-134">Specifies the name of the server to which to restore a database.</span></span>
<span data-ttu-id="f137c-135">Você pode restaurar um banco de dados para o mesmo servidor ou para um servidor diferente.</span><span class="sxs-lookup"><span data-stu-id="f137c-135">You can restore a database to the same server or to a different server.</span></span>

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

### <span data-ttu-id="f137c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f137c-136">CommonParameters</span></span>
<span data-ttu-id="f137c-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f137c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f137c-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f137c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f137c-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f137c-139">INPUTS</span></span>

### <span data-ttu-id="f137c-140">Microsoft. WindowsAzure. Management. Sql. Models. RecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="f137c-140">Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase</span></span>

## <span data-ttu-id="f137c-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f137c-141">OUTPUTS</span></span>

### <span data-ttu-id="f137c-142">Microsoft. WindowsAzure. Management. Sql. Models. RecoverDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="f137c-142">Microsoft.WindowsAzure.Management.Sql.Models.RecoverDatabaseOperation</span></span>

## <span data-ttu-id="f137c-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f137c-143">NOTES</span></span>
* <span data-ttu-id="f137c-144">Você deve usar a autenticação baseada em certificado para executar esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f137c-144">You must use certificate-based authentication to run this cmdlet.</span></span> <span data-ttu-id="f137c-145">Execute os seguintes comandos no computador em que você executa este cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f137c-145">Run the following commands on the computer where you run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="f137c-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f137c-146">RELATED LINKS</span></span>

[<span data-ttu-id="f137c-147">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="f137c-147">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="f137c-148">Criar solicitação de recuperação de banco de dados</span><span class="sxs-lookup"><span data-stu-id="f137c-148">Create Database Recovery Request</span></span>](https://msdn.microsoft.com/en-us/library/dn800986.aspx)

[<span data-ttu-id="f137c-149">Replicação geográfica no banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="f137c-149">Geo-Replication in Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/)

[<span data-ttu-id="f137c-150">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="f137c-150">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="f137c-151">Get-AzureSqlRecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="f137c-151">Get-AzureSqlRecoverableDatabase</span></span>](./Get-AzureSqlRecoverableDatabase.md)

[<span data-ttu-id="f137c-152">Start-AzureSqlDatabaseRestore</span><span class="sxs-lookup"><span data-stu-id="f137c-152">Start-AzureSqlDatabaseRestore</span></span>](./Start-AzureSqlDatabaseRestore.md)


