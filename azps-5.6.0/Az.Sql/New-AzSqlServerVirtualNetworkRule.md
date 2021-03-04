---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: f5dbea3701f7f0fdaf9c503e58e03fdcc9237530
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885785"
---
# <span data-ttu-id="626ef-101">New-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="626ef-101">New-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="626ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="626ef-102">SYNOPSIS</span></span>
<span data-ttu-id="626ef-103">Cria uma regra de rede virtual do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="626ef-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

## <span data-ttu-id="626ef-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="626ef-104">SYNTAX</span></span>

```
New-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="626ef-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="626ef-105">DESCRIPTION</span></span>
<span data-ttu-id="626ef-106">Cria uma regra de rede virtual do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="626ef-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="626ef-107">As Regras de Rede Virtual são usadas para conectar o SQL Server do Azure a uma Rede Virtual específica para restringir o acesso no SQL Server do Azure para estar disponível apenas na Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="626ef-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="626ef-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="626ef-108">EXAMPLES</span></span>

### <span data-ttu-id="626ef-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="626ef-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="626ef-110">Cria uma regra de SQL Server de rede virtual do Azure</span><span class="sxs-lookup"><span data-stu-id="626ef-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="626ef-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="626ef-111">PARAMETERS</span></span>

### <span data-ttu-id="626ef-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="626ef-112">-AsJob</span></span>
<span data-ttu-id="626ef-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="626ef-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="626ef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="626ef-114">-DefaultProfile</span></span>
<span data-ttu-id="626ef-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="626ef-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="626ef-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="626ef-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="626ef-117">Criar regra de firewall antes que a rede virtual tenha o ponto de extremidade do serviço vnet habilitado.</span><span class="sxs-lookup"><span data-stu-id="626ef-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="626ef-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="626ef-118">-ResourceGroupName</span></span>
<span data-ttu-id="626ef-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="626ef-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="626ef-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="626ef-120">-ServerName</span></span>
<span data-ttu-id="626ef-121">O nome do Sql Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="626ef-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="626ef-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="626ef-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="626ef-123">Nome da regra de rede virtual do Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="626ef-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="626ef-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="626ef-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="626ef-125">A ID da Sub-rede de Rede Virtual que especifica os detalhes da Microsoft.Network</span><span class="sxs-lookup"><span data-stu-id="626ef-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="626ef-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="626ef-126">-Confirm</span></span>
<span data-ttu-id="626ef-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="626ef-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="626ef-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="626ef-128">-WhatIf</span></span>
<span data-ttu-id="626ef-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="626ef-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="626ef-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="626ef-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="626ef-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="626ef-131">CommonParameters</span></span>
<span data-ttu-id="626ef-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="626ef-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="626ef-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="626ef-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="626ef-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="626ef-134">INPUTS</span></span>

### <span data-ttu-id="626ef-135">System.String</span><span class="sxs-lookup"><span data-stu-id="626ef-135">System.String</span></span>

## <span data-ttu-id="626ef-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="626ef-136">OUTPUTS</span></span>

### <span data-ttu-id="626ef-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="626ef-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="626ef-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="626ef-138">NOTES</span></span>

## <span data-ttu-id="626ef-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="626ef-139">RELATED LINKS</span></span>
