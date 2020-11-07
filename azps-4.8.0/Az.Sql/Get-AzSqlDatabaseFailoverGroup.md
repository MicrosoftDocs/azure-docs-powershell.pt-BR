---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a2c7192fc1ce2055b05a4f943a0c04560f1e714e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954643"
---
# <span data-ttu-id="9f152-101">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9f152-101">Get-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="9f152-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f152-102">SYNOPSIS</span></span>
<span data-ttu-id="9f152-103">Obtém ou lista os grupos de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f152-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

## <span data-ttu-id="9f152-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f152-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f152-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9f152-105">DESCRIPTION</span></span>
<span data-ttu-id="9f152-106">Obtém um grupo específico de failover de banco de dados SQL do Azure ou lista os grupos de failover em um servidor.</span><span class="sxs-lookup"><span data-stu-id="9f152-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="9f152-107">Qualquer servidor no grupo de failover pode ser usado para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="9f152-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="9f152-108">Os valores retornados refletirão o estado do servidor especificado em relação ao grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="9f152-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="9f152-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f152-109">EXAMPLES</span></span>

### <span data-ttu-id="9f152-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9f152-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="9f152-111">Lista todos os grupos de failover em um servidor.</span><span class="sxs-lookup"><span data-stu-id="9f152-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="9f152-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9f152-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="9f152-113">Obter um grupo específico de failover.</span><span class="sxs-lookup"><span data-stu-id="9f152-113">Get a specific Failover Group.</span></span>

### <span data-ttu-id="9f152-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="9f152-114">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

<span data-ttu-id="9f152-115">Obtenha todos os grupos de failover em um servidor que comece com "FG".</span><span class="sxs-lookup"><span data-stu-id="9f152-115">Get all failover groups in a server that start with "fg".</span></span>

## <span data-ttu-id="9f152-116">OS</span><span class="sxs-lookup"><span data-stu-id="9f152-116">PARAMETERS</span></span>

### <span data-ttu-id="9f152-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f152-117">-DefaultProfile</span></span>
<span data-ttu-id="9f152-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9f152-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f152-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="9f152-119">-FailoverGroupName</span></span>
<span data-ttu-id="9f152-120">O nome do grupo de failover de banco de dados SQL do Azure a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="9f152-120">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

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

### <span data-ttu-id="9f152-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f152-121">-ResourceGroupName</span></span>
<span data-ttu-id="9f152-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9f152-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="9f152-123">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="9f152-123">-ServerName</span></span>
<span data-ttu-id="9f152-124">O nome do servidor de banco de dados SQL do Azure do qual recuperar o grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="9f152-124">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="9f152-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f152-125">CommonParameters</span></span>
<span data-ttu-id="9f152-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f152-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f152-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f152-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f152-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9f152-128">INPUTS</span></span>

### <span data-ttu-id="9f152-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9f152-129">System.String</span></span>

## <span data-ttu-id="9f152-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9f152-130">OUTPUTS</span></span>

### <span data-ttu-id="9f152-131">Microsoft. Azure. Commands. Sql. failover. Model. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="9f152-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="9f152-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9f152-132">NOTES</span></span>

## <span data-ttu-id="9f152-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f152-133">RELATED LINKS</span></span>

[<span data-ttu-id="9f152-134">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9f152-134">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9f152-135">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9f152-135">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9f152-136">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9f152-136">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="9f152-137">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9f152-137">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="9f152-138">Botão de AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9f152-138">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9f152-139">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9f152-139">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9f152-140">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="9f152-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
