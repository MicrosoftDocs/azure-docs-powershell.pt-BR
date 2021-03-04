---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: f4744eee1e93867ea150819a8f4bcadc5ac8a35b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892035"
---
# <span data-ttu-id="80b61-101">Get-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="80b61-101">Get-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="80b61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80b61-102">SYNOPSIS</span></span>
<span data-ttu-id="80b61-103">Obtém ou lista o Azure SQL Server Regra de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="80b61-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="80b61-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="80b61-104">SYNTAX</span></span>

```
Get-AzSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80b61-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="80b61-105">DESCRIPTION</span></span>
<span data-ttu-id="80b61-106">Este comando obtém uma Regra de Rede Virtual específica do Azure SQL Server ou uma lista de regras de rede virtual do Azure SQL Server em um servidor.</span><span class="sxs-lookup"><span data-stu-id="80b61-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="80b61-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80b61-107">EXAMPLES</span></span>

### <span data-ttu-id="80b61-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="80b61-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="80b61-109">Obtém uma única regra de SQL Server de rede virtual do Azure</span><span class="sxs-lookup"><span data-stu-id="80b61-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="80b61-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="80b61-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="80b61-111">Obtém a lista de regras SQL Server de rede virtual do Azure no servidor especificado</span><span class="sxs-lookup"><span data-stu-id="80b61-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

### <span data-ttu-id="80b61-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="80b61-112">Example 3</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRule*
```

<span data-ttu-id="80b61-113">Obtém a lista de regras de rede virtual do Azure SQL Server no servidor especificado que começa com "virtualNetworkRule".</span><span class="sxs-lookup"><span data-stu-id="80b61-113">Gets the list of Azure SQL Server virtual network rules under the specified server that start with "virtualNetworkRule".</span></span>

## <span data-ttu-id="80b61-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="80b61-114">PARAMETERS</span></span>

### <span data-ttu-id="80b61-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80b61-115">-DefaultProfile</span></span>
<span data-ttu-id="80b61-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="80b61-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80b61-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80b61-117">-ResourceGroupName</span></span>
<span data-ttu-id="80b61-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="80b61-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="80b61-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="80b61-119">-ServerName</span></span>
<span data-ttu-id="80b61-120">O nome do Sql Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="80b61-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="80b61-121">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="80b61-121">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="80b61-122">O nome da Regra de Rede Virtual do Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="80b61-122">The Azure Sql Server Virtual Network Rule name.</span></span>

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

### <span data-ttu-id="80b61-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80b61-123">CommonParameters</span></span>
<span data-ttu-id="80b61-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80b61-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80b61-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80b61-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80b61-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80b61-126">INPUTS</span></span>

### <span data-ttu-id="80b61-127">System.String</span><span class="sxs-lookup"><span data-stu-id="80b61-127">System.String</span></span>

## <span data-ttu-id="80b61-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="80b61-128">OUTPUTS</span></span>

### <span data-ttu-id="80b61-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="80b61-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="80b61-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="80b61-130">NOTES</span></span>

## <span data-ttu-id="80b61-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80b61-131">RELATED LINKS</span></span>
