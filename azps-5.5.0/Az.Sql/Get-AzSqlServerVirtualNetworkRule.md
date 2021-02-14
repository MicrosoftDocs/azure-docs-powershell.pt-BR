---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: f8ac34526691f3bdacdd0736189e063c969f63ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111328"
---
# <span data-ttu-id="3191f-101">Get-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3191f-101">Get-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="3191f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3191f-102">SYNOPSIS</span></span>
<span data-ttu-id="3191f-103">Obtém ou lista a Regra de Rede Virtual do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3191f-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="3191f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3191f-104">SYNTAX</span></span>

```
Get-AzSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3191f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3191f-105">DESCRIPTION</span></span>
<span data-ttu-id="3191f-106">Esse comando obtém uma Regra de Rede Virtual do Azure SQL Server específica ou uma lista de Regras de Rede Virtual do Azure SQL Server em um servidor.</span><span class="sxs-lookup"><span data-stu-id="3191f-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="3191f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3191f-107">EXAMPLES</span></span>

### <span data-ttu-id="3191f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3191f-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="3191f-109">Obtém uma única regra de rede virtual do SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="3191f-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="3191f-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3191f-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="3191f-111">Obtém a lista de regras de rede virtual do SQL Server do Azure no servidor especificado</span><span class="sxs-lookup"><span data-stu-id="3191f-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

### <span data-ttu-id="3191f-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="3191f-112">Example 3</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRule*
```

<span data-ttu-id="3191f-113">Obtém a lista de regras de rede virtual do SQL Server do Azure no servidor especificado que começam com "virtualNetworkRule".</span><span class="sxs-lookup"><span data-stu-id="3191f-113">Gets the list of Azure SQL Server virtual network rules under the specified server that start with "virtualNetworkRule".</span></span>

## <span data-ttu-id="3191f-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3191f-114">PARAMETERS</span></span>

### <span data-ttu-id="3191f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3191f-115">-DefaultProfile</span></span>
<span data-ttu-id="3191f-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3191f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3191f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3191f-117">-ResourceGroupName</span></span>
<span data-ttu-id="3191f-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3191f-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="3191f-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3191f-119">-ServerName</span></span>
<span data-ttu-id="3191f-120">O nome do Sql Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="3191f-120">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3191f-121">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="3191f-121">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="3191f-122">O nome da Regra de Rede Virtual do Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="3191f-122">The Azure Sql Server Virtual Network Rule name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3191f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3191f-123">CommonParameters</span></span>
<span data-ttu-id="3191f-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3191f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3191f-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3191f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3191f-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="3191f-126">INPUTS</span></span>

### <span data-ttu-id="3191f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="3191f-127">System.String</span></span>

## <span data-ttu-id="3191f-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="3191f-128">OUTPUTS</span></span>

### <span data-ttu-id="3191f-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="3191f-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="3191f-130">Notas</span><span class="sxs-lookup"><span data-stu-id="3191f-130">NOTES</span></span>

## <span data-ttu-id="3191f-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3191f-131">RELATED LINKS</span></span>
