---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: f8ac34526691f3bdacdd0736189e063c969f63ff
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281708"
---
# <span data-ttu-id="cdad7-101">Get-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cdad7-101">Get-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="cdad7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cdad7-102">SYNOPSIS</span></span>
<span data-ttu-id="cdad7-103">Obtém ou lista a regra de rede virtual do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cdad7-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="cdad7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cdad7-104">SYNTAX</span></span>

```
Get-AzSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdad7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cdad7-105">DESCRIPTION</span></span>
<span data-ttu-id="cdad7-106">Esse comando obtém uma regra específica de rede virtual do SQL Server do Azure ou uma lista de regras de rede virtual do Azure SQL Server em um servidor.</span><span class="sxs-lookup"><span data-stu-id="cdad7-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="cdad7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cdad7-107">EXAMPLES</span></span>

### <span data-ttu-id="cdad7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cdad7-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="cdad7-109">Obtém uma única regra de rede virtual do Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="cdad7-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="cdad7-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cdad7-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="cdad7-111">Obtém a lista de regras de rede virtual do Azure SQL Server no servidor especificado</span><span class="sxs-lookup"><span data-stu-id="cdad7-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

### <span data-ttu-id="cdad7-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="cdad7-112">Example 3</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRule*
```

<span data-ttu-id="cdad7-113">Obtém a lista de regras de rede virtual do Azure SQL Server no servidor especificado que começa com "virtualNetworkRule".</span><span class="sxs-lookup"><span data-stu-id="cdad7-113">Gets the list of Azure SQL Server virtual network rules under the specified server that start with "virtualNetworkRule".</span></span>

## <span data-ttu-id="cdad7-114">OS</span><span class="sxs-lookup"><span data-stu-id="cdad7-114">PARAMETERS</span></span>

### <span data-ttu-id="cdad7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdad7-115">-DefaultProfile</span></span>
<span data-ttu-id="cdad7-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cdad7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cdad7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdad7-117">-ResourceGroupName</span></span>
<span data-ttu-id="cdad7-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cdad7-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="cdad7-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="cdad7-119">-ServerName</span></span>
<span data-ttu-id="cdad7-120">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="cdad7-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="cdad7-121">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="cdad7-121">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="cdad7-122">O nome da regra de rede virtual do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="cdad7-122">The Azure Sql Server Virtual Network Rule name.</span></span>

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

### <span data-ttu-id="cdad7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdad7-123">CommonParameters</span></span>
<span data-ttu-id="cdad7-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdad7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdad7-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cdad7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdad7-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cdad7-126">INPUTS</span></span>

### <span data-ttu-id="cdad7-127">System. String</span><span class="sxs-lookup"><span data-stu-id="cdad7-127">System.String</span></span>

## <span data-ttu-id="cdad7-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cdad7-128">OUTPUTS</span></span>

### <span data-ttu-id="cdad7-129">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="cdad7-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="cdad7-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cdad7-130">NOTES</span></span>

## <span data-ttu-id="cdad7-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cdad7-131">RELATED LINKS</span></span>
