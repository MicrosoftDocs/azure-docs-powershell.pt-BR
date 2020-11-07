---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 6723557D-8052-4BFA-872C-384B1423B3AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185ad06375fe9bbd11cb25c26b25704baeaa1dfe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945570"
---
# <span data-ttu-id="69f85-101">Get-AzureSqlDatabaseServerQuota</span><span class="sxs-lookup"><span data-stu-id="69f85-101">Get-AzureSqlDatabaseServerQuota</span></span>

## <span data-ttu-id="69f85-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69f85-102">SYNOPSIS</span></span>
<span data-ttu-id="69f85-103">Obtém informações de cota para um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="69f85-103">Gets quota information for an Azure SQL Database server.</span></span>

## <span data-ttu-id="69f85-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69f85-104">SYNTAX</span></span>

### <span data-ttu-id="69f85-105">ByConnectionContext</span><span class="sxs-lookup"><span data-stu-id="69f85-105">ByConnectionContext</span></span>
```
Get-AzureSqlDatabaseServerQuota -ConnectionContext <IServerDataServiceContext> [-QuotaName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="69f85-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="69f85-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseServerQuota -ServerName <String> [-QuotaName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="69f85-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69f85-107">DESCRIPTION</span></span>
<span data-ttu-id="69f85-108">O cmdlet **Get-AzureSqlDatabaseServerQuota** Obtém as informações de cota de uma instância especificada do servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="69f85-108">The **Get-AzureSqlDatabaseServerQuota** cmdlet gets the quota information for a specified instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="69f85-109">Especifique um contexto de conexão ou o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="69f85-109">Specify a connection context or the server name.</span></span>
<span data-ttu-id="69f85-110">Se você não especificar um nome de cota, esse cmdlet obtém todas as informações de cota do servidor.</span><span class="sxs-lookup"><span data-stu-id="69f85-110">If you do not specify a quota name, this cmdlet gets all the quota information for the server.</span></span>

## <span data-ttu-id="69f85-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69f85-111">EXAMPLES</span></span>

### <span data-ttu-id="69f85-112">Exemplo 1: obter informações para uma cota específica</span><span class="sxs-lookup"><span data-stu-id="69f85-112">Example 1: Get information for a specific quota</span></span>
```
PS C:\> $QuotaPremium = GetAzureSqlDatabaseServerQuota $Context -QuotaName "Premium_Databases"
```

<span data-ttu-id="69f85-113">Esse comando obtém a cota chamada Premium_Databases do servidor de banco de dados SQL do Azure especificado pela conexão armazenada na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="69f85-113">This command gets the quota named Premium_Databases from the Azure SQL Database server specified by the connection stored in the $Context variable.</span></span>

### <span data-ttu-id="69f85-114">Exemplo 2: obter informações para todas as cotas</span><span class="sxs-lookup"><span data-stu-id="69f85-114">Example 2: Get information for all quotas</span></span>
```
PS C:\> $QuotaList = GetAzureSqlDatabaseServerQuota $Context
```

<span data-ttu-id="69f85-115">Esse comando obtém todos os valores de cota do servidor especificado pela $Context de conexão.</span><span class="sxs-lookup"><span data-stu-id="69f85-115">This command gets all quota values from the server specified by the connection $Context.</span></span>

## <span data-ttu-id="69f85-116">OS</span><span class="sxs-lookup"><span data-stu-id="69f85-116">PARAMETERS</span></span>

### <span data-ttu-id="69f85-117">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="69f85-117">-ConnectionContext</span></span>
<span data-ttu-id="69f85-118">Especifica o contexto de conexão de um servidor.</span><span class="sxs-lookup"><span data-stu-id="69f85-118">Specifies the connection context of a server.</span></span>

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

### <span data-ttu-id="69f85-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="69f85-119">-Profile</span></span>
<span data-ttu-id="69f85-120">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="69f85-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="69f85-121">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="69f85-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="69f85-122">-Quotaname</span><span class="sxs-lookup"><span data-stu-id="69f85-122">-QuotaName</span></span>
<span data-ttu-id="69f85-123">Especifica o nome do valor de cota que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="69f85-123">Specifies the name of the quota value that this cmdlet gets.</span></span>

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

### <span data-ttu-id="69f85-124">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="69f85-124">-ServerName</span></span>
<span data-ttu-id="69f85-125">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="69f85-125">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="69f85-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69f85-126">CommonParameters</span></span>
<span data-ttu-id="69f85-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69f85-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69f85-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69f85-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69f85-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69f85-129">INPUTS</span></span>

## <span data-ttu-id="69f85-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69f85-130">OUTPUTS</span></span>

### <span data-ttu-id="69f85-131">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. ServerQuota []</span><span class="sxs-lookup"><span data-stu-id="69f85-131">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServerQuota[]</span></span>

## <span data-ttu-id="69f85-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69f85-132">NOTES</span></span>
* <span data-ttu-id="69f85-133">Autenticação: esse cmdlet pode usar a autenticação do SQL Server ou da autenticação baseada em certificados.</span><span class="sxs-lookup"><span data-stu-id="69f85-133">Authentication: This cmdlet can use either SQL Server authentication or certificate-based authentication.</span></span> <span data-ttu-id="69f85-134">Para obter exemplos de como configurar a autenticação, consulte o cmdlet New-AzureSqlDatabaseServerContext.</span><span class="sxs-lookup"><span data-stu-id="69f85-134">For examples of setting up authentication, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="69f85-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69f85-135">RELATED LINKS</span></span>

[<span data-ttu-id="69f85-136">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="69f85-136">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="69f85-137">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="69f85-137">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="69f85-138">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="69f85-138">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


