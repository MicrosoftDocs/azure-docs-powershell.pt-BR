---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 83E8DAD8-151A-408D-819F-274CB813ABDA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6f9a5753fdf4f87afc6baacbe9fc4c33c9be08ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946559"
---
# <span data-ttu-id="c1bf4-101">Get-AzureSqlRecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="c1bf4-101">Get-AzureSqlRecoverableDatabase</span></span>

## <span data-ttu-id="c1bf4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="c1bf4-103">Obtém bancos de dados recuperáveis de um servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="c1bf4-103">Gets recoverable databases from a specified server.</span></span>

## <span data-ttu-id="c1bf4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1bf4-104">SYNTAX</span></span>

### <span data-ttu-id="c1bf4-105">AllDatabasesOnGivenServer (padrão)</span><span class="sxs-lookup"><span data-stu-id="c1bf4-105">AllDatabasesOnGivenServer (Default)</span></span>
```
Get-AzureSqlRecoverableDatabase -ServerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c1bf4-106">GivenDatabaseOnGivenServer</span><span class="sxs-lookup"><span data-stu-id="c1bf4-106">GivenDatabaseOnGivenServer</span></span>
```
Get-AzureSqlRecoverableDatabase -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1bf4-107">GivenDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="c1bf4-107">GivenDatabaseObject</span></span>
```
Get-AzureSqlRecoverableDatabase -Database <RecoverableDatabase> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1bf4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1bf4-108">DESCRIPTION</span></span>
<span data-ttu-id="c1bf4-109">O cmdlet **Get-AzureSqlRecoverableDatabase** Obtém bancos de dados recuperáveis de um servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="c1bf4-109">The **Get-AzureSqlRecoverableDatabase** cmdlet gets recoverable databases from a specified server.</span></span>
<span data-ttu-id="c1bf4-110">Esse cmdlet obtém um banco de dados recuperável específico ou todos os bancos de dados recuperáveis em um servidor.</span><span class="sxs-lookup"><span data-stu-id="c1bf4-110">This cmdlet gets a specific recoverable database or all recoverable databases on a server.</span></span>

## <span data-ttu-id="c1bf4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1bf4-111">EXAMPLES</span></span>

### <span data-ttu-id="c1bf4-112">Exemplo 1: obter todos os bancos de dados recuperáveis</span><span class="sxs-lookup"><span data-stu-id="c1bf4-112">Example 1: Get all recoverable databases</span></span>
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01"
```

<span data-ttu-id="c1bf4-113">Esse comando obtém todos os bancos de dados recuperáveis no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="c1bf4-113">This command gets all recoverable databases on the server named Server01.</span></span>

### <span data-ttu-id="c1bf4-114">Exemplo 2: obter um banco de dados recuperável específico</span><span class="sxs-lookup"><span data-stu-id="c1bf4-114">Example 2: Get a specific recoverable database</span></span>
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17"
```

<span data-ttu-id="c1bf4-115">Esse comando é recuperado o banco de dados chamado Database17 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="c1bf4-115">This command gets retrieves the database named Database17 on the server named Server01.</span></span>

## <span data-ttu-id="c1bf4-116">OS</span><span class="sxs-lookup"><span data-stu-id="c1bf4-116">PARAMETERS</span></span>

### <span data-ttu-id="c1bf4-117">-Banco de dados</span><span class="sxs-lookup"><span data-stu-id="c1bf4-117">-Database</span></span>
<span data-ttu-id="c1bf4-118">Especifica um objeto que representa o banco de dados recuperável que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="c1bf4-118">Specifies an object that represents the recoverable database that this cmdlet gets.</span></span>

```yaml
Type: RecoverableDatabase
Parameter Sets: GivenDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1bf4-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c1bf4-119">-DatabaseName</span></span>
<span data-ttu-id="c1bf4-120">Especifica o nome do banco de dados recuperável que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="c1bf4-120">Specifies the name of the recoverable database that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GivenDatabaseOnGivenServer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1bf4-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c1bf4-121">-Profile</span></span>
<span data-ttu-id="c1bf4-122">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="c1bf4-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c1bf4-123">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="c1bf4-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c1bf4-124">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="c1bf4-124">-ServerName</span></span>
<span data-ttu-id="c1bf4-125">Especifica o nome do servidor do qual esse cmdlet obtém bancos de dados recuperáveis.</span><span class="sxs-lookup"><span data-stu-id="c1bf4-125">Specifies the name of the server from which this cmdlet gets recoverable databases.</span></span>

```yaml
Type: String
Parameter Sets: AllDatabasesOnGivenServer, GivenDatabaseOnGivenServer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1bf4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1bf4-126">CommonParameters</span></span>
<span data-ttu-id="c1bf4-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1bf4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1bf4-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1bf4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1bf4-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1bf4-129">INPUTS</span></span>

### <span data-ttu-id="c1bf4-130">Microsoft. WindowsAzure. Management. Sql. Models. RecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="c1bf4-130">Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase</span></span>

## <span data-ttu-id="c1bf4-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1bf4-131">OUTPUTS</span></span>

### <span data-ttu-id="c1bf4-132">IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\></span><span class="sxs-lookup"><span data-stu-id="c1bf4-132">IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\></span></span>

## <span data-ttu-id="c1bf4-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1bf4-133">NOTES</span></span>
* <span data-ttu-id="c1bf4-134">Você deve usar a autenticação baseada em certificado para executar esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1bf4-134">You must use certificate-based authentication to run this cmdlet.</span></span> <span data-ttu-id="c1bf4-135">Execute os seguintes comandos no computador onde executar este cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c1bf4-135">Run the following commands on the computer where run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="c1bf4-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1bf4-136">RELATED LINKS</span></span>

[<span data-ttu-id="c1bf4-137">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="c1bf4-137">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="c1bf4-138">Obter banco de dados recuperável</span><span class="sxs-lookup"><span data-stu-id="c1bf4-138">Get Recoverable Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn800985.aspx)

[<span data-ttu-id="c1bf4-139">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="c1bf4-139">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="c1bf4-140">Start-AzureSqlDatabaseRecovery</span><span class="sxs-lookup"><span data-stu-id="c1bf4-140">Start-AzureSqlDatabaseRecovery</span></span>](./Start-AzureSqlDatabaseRecovery.md)


