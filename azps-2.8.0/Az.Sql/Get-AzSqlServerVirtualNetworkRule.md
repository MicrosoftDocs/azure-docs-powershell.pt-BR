---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 3e9b99a1ab9d3fdce813166e7a0834c14b81b651
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773591"
---
# <span data-ttu-id="52db1-101">Get-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="52db1-101">Get-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="52db1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52db1-102">SYNOPSIS</span></span>
<span data-ttu-id="52db1-103">Obtém ou lista a regra de rede virtual do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="52db1-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="52db1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52db1-104">SYNTAX</span></span>

```
Get-AzSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52db1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52db1-105">DESCRIPTION</span></span>
<span data-ttu-id="52db1-106">Esse comando obtém uma regra específica de rede virtual do SQL Server do Azure ou uma lista de regras de rede virtual do Azure SQL Server em um servidor.</span><span class="sxs-lookup"><span data-stu-id="52db1-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="52db1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52db1-107">EXAMPLES</span></span>

### <span data-ttu-id="52db1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52db1-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="52db1-109">Obtém uma única regra de rede virtual do Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="52db1-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="52db1-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="52db1-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="52db1-111">Obtém a lista de regras de rede virtual do Azure SQL Server no servidor especificado</span><span class="sxs-lookup"><span data-stu-id="52db1-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

### <span data-ttu-id="52db1-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="52db1-112">Example 3</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRule*
```

<span data-ttu-id="52db1-113">Obtém a lista de regras de rede virtual do Azure SQL Server no servidor especificado que começa com "virtualNetworkRule".</span><span class="sxs-lookup"><span data-stu-id="52db1-113">Gets the list of Azure SQL Server virtual network rules under the specified server that start with "virtualNetworkRule".</span></span>

## <span data-ttu-id="52db1-114">OS</span><span class="sxs-lookup"><span data-stu-id="52db1-114">PARAMETERS</span></span>

### <span data-ttu-id="52db1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52db1-115">-DefaultProfile</span></span>
<span data-ttu-id="52db1-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="52db1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52db1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52db1-117">-ResourceGroupName</span></span>
<span data-ttu-id="52db1-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="52db1-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="52db1-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="52db1-119">-ServerName</span></span>
<span data-ttu-id="52db1-120">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="52db1-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="52db1-121">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="52db1-121">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="52db1-122">O nome da regra de rede virtual do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="52db1-122">The Azure Sql Server Virtual Network Rule name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="52db1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52db1-123">CommonParameters</span></span>
<span data-ttu-id="52db1-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52db1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52db1-125">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52db1-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52db1-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52db1-126">INPUTS</span></span>

### <span data-ttu-id="52db1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="52db1-127">System.String</span></span>

## <span data-ttu-id="52db1-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52db1-128">OUTPUTS</span></span>

### <span data-ttu-id="52db1-129">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="52db1-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="52db1-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52db1-130">NOTES</span></span>

## <span data-ttu-id="52db1-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52db1-131">RELATED LINKS</span></span>
