---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: b583c8339ebec74fdf8df4116204b7ad5523c258
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891276"
---
# <span data-ttu-id="b19d5-101">Set-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b19d5-101">Set-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="b19d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b19d5-102">SYNOPSIS</span></span>
<span data-ttu-id="b19d5-103">Modifica a configuração de uma regra de rede virtual do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b19d5-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="b19d5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b19d5-104">SYNTAX</span></span>

```
Set-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b19d5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b19d5-105">DESCRIPTION</span></span>
<span data-ttu-id="b19d5-106">Este comando modifica a configuração de uma Regra de Rede Virtual do Azure SQL Server Virtual.</span><span class="sxs-lookup"><span data-stu-id="b19d5-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="b19d5-107">Para controlar o conjunto de regras de rede virtual no servidor, use 'Add-AzSqlServerVirtualNetworkRule' e 'Remove-AzSqlServerVirtualNetworkRule' em vez disso.</span><span class="sxs-lookup"><span data-stu-id="b19d5-107">To control the set of virtual network rules in the server, use 'Add-AzSqlServerVirtualNetworkRule' and 'Remove-AzSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="b19d5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b19d5-108">EXAMPLES</span></span>

### <span data-ttu-id="b19d5-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b19d5-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="b19d5-110">Modifica uma regra de rede virtual existente com a nova id de sub-rede de rede virtual que contém informações sobre a nova rede virtual</span><span class="sxs-lookup"><span data-stu-id="b19d5-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="b19d5-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b19d5-111">PARAMETERS</span></span>

### <span data-ttu-id="b19d5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b19d5-112">-AsJob</span></span>
<span data-ttu-id="b19d5-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b19d5-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b19d5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b19d5-114">-DefaultProfile</span></span>
<span data-ttu-id="b19d5-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b19d5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b19d5-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b19d5-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="b19d5-117">Criar regra de firewall antes que a rede virtual tenha o ponto de extremidade do serviço vnet habilitado.</span><span class="sxs-lookup"><span data-stu-id="b19d5-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="b19d5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b19d5-118">-ResourceGroupName</span></span>
<span data-ttu-id="b19d5-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b19d5-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="b19d5-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b19d5-120">-ServerName</span></span>
<span data-ttu-id="b19d5-121">O nome do Sql Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="b19d5-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="b19d5-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="b19d5-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="b19d5-123">O nome da Regra de Rede Virtual do Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="b19d5-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="b19d5-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="b19d5-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="b19d5-125">A ID da Sub-rede de Rede Virtual da regra.</span><span class="sxs-lookup"><span data-stu-id="b19d5-125">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="b19d5-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b19d5-126">-Confirm</span></span>
<span data-ttu-id="b19d5-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b19d5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b19d5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b19d5-128">-WhatIf</span></span>
<span data-ttu-id="b19d5-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b19d5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b19d5-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b19d5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b19d5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b19d5-131">CommonParameters</span></span>
<span data-ttu-id="b19d5-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b19d5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b19d5-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b19d5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b19d5-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b19d5-134">INPUTS</span></span>

### <span data-ttu-id="b19d5-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b19d5-135">System.String</span></span>

## <span data-ttu-id="b19d5-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b19d5-136">OUTPUTS</span></span>

### <span data-ttu-id="b19d5-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="b19d5-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="b19d5-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="b19d5-138">NOTES</span></span>

## <span data-ttu-id="b19d5-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b19d5-139">RELATED LINKS</span></span>
