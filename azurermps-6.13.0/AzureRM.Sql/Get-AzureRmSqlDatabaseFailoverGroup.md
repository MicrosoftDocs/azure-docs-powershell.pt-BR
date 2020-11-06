---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: db85c1f8de00432b3f9213473c89728239099c0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429314"
---
# <span data-ttu-id="01a32-101">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="01a32-101">Get-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="01a32-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01a32-102">SYNOPSIS</span></span>
<span data-ttu-id="01a32-103">Obtém ou lista os grupos de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="01a32-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01a32-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01a32-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01a32-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="01a32-105">DESCRIPTION</span></span>
<span data-ttu-id="01a32-106">Obtém um grupo específico de failover de banco de dados SQL do Azure ou lista os grupos de failover em um servidor.</span><span class="sxs-lookup"><span data-stu-id="01a32-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="01a32-107">Qualquer servidor no grupo de failover pode ser usado para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="01a32-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="01a32-108">Os valores retornados refletirão o estado do servidor especificado em relação ao grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="01a32-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="01a32-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="01a32-109">EXAMPLES</span></span>

### <span data-ttu-id="01a32-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="01a32-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="01a32-111">Lista todos os grupos de failover em um servidor.</span><span class="sxs-lookup"><span data-stu-id="01a32-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="01a32-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="01a32-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="01a32-113">Obter um grupo específico de failover.</span><span class="sxs-lookup"><span data-stu-id="01a32-113">Get a specific Failover Group.</span></span>

## <span data-ttu-id="01a32-114">OS</span><span class="sxs-lookup"><span data-stu-id="01a32-114">PARAMETERS</span></span>

### <span data-ttu-id="01a32-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01a32-115">-DefaultProfile</span></span>
<span data-ttu-id="01a32-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="01a32-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a32-117">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="01a32-117">-FailoverGroupName</span></span>
<span data-ttu-id="01a32-118">O nome do grupo de failover de banco de dados SQL do Azure a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="01a32-118">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a32-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01a32-119">-ResourceGroupName</span></span>
<span data-ttu-id="01a32-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="01a32-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a32-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="01a32-121">-ServerName</span></span>
<span data-ttu-id="01a32-122">O nome do servidor de banco de dados SQL do Azure do qual recuperar o grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="01a32-122">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a32-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01a32-123">CommonParameters</span></span>
<span data-ttu-id="01a32-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01a32-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01a32-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01a32-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01a32-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="01a32-126">INPUTS</span></span>

### <span data-ttu-id="01a32-127">System. String</span><span class="sxs-lookup"><span data-stu-id="01a32-127">System.String</span></span>

## <span data-ttu-id="01a32-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="01a32-128">OUTPUTS</span></span>

### <span data-ttu-id="01a32-129">Microsoft. Azure. Commands. Sql. failover. Model. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="01a32-129">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="01a32-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="01a32-130">NOTES</span></span>

## <span data-ttu-id="01a32-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01a32-131">RELATED LINKS</span></span>

[<span data-ttu-id="01a32-132">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="01a32-132">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="01a32-133">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="01a32-133">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="01a32-134">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="01a32-134">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="01a32-135">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="01a32-135">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="01a32-136">Botão de AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="01a32-136">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="01a32-137">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="01a32-137">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="01a32-138">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="01a32-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
