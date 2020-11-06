---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 3b318e08e4dbf900b54581b18f551a3accb75480
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598745"
---
# <span data-ttu-id="b71d4-101">Set-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b71d4-101">Set-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="b71d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b71d4-102">SYNOPSIS</span></span>
<span data-ttu-id="b71d4-103">Modifica a configuração de uma regra de rede virtual do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b71d4-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="b71d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b71d4-104">SYNTAX</span></span>

```
Set-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b71d4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b71d4-105">DESCRIPTION</span></span>
<span data-ttu-id="b71d4-106">Esse comando modifica a configuração de uma regra de rede virtual do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b71d4-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="b71d4-107">Para controlar o conjunto de regras de rede virtual no servidor, use "Add-AzSqlServerVirtualNetworkRule" e "Remove-AzSqlServerVirtualNetworkRule" em vez disso.</span><span class="sxs-lookup"><span data-stu-id="b71d4-107">To control the set of virtual network rules in the server, use 'Add-AzSqlServerVirtualNetworkRule' and 'Remove-AzSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="b71d4-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b71d4-108">EXAMPLES</span></span>

### <span data-ttu-id="b71d4-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b71d4-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="b71d4-110">Modifica uma regra de rede virtual existente com a nova ID de sub-rede de rede virtual que contém informações sobre a nova rede virtual</span><span class="sxs-lookup"><span data-stu-id="b71d4-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="b71d4-111">OS</span><span class="sxs-lookup"><span data-stu-id="b71d4-111">PARAMETERS</span></span>

### <span data-ttu-id="b71d4-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b71d4-112">-AsJob</span></span>
<span data-ttu-id="b71d4-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b71d4-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b71d4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b71d4-114">-DefaultProfile</span></span>
<span data-ttu-id="b71d4-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b71d4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b71d4-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b71d4-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="b71d4-117">Crie uma regra de firewall antes da rede virtual ter ponto de extremidade do serviço vnet habilitado.</span><span class="sxs-lookup"><span data-stu-id="b71d4-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="b71d4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b71d4-118">-ResourceGroupName</span></span>
<span data-ttu-id="b71d4-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b71d4-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="b71d4-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="b71d4-120">-ServerName</span></span>
<span data-ttu-id="b71d4-121">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="b71d4-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="b71d4-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="b71d4-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="b71d4-123">O nome da regra de rede virtual do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b71d4-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="b71d4-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="b71d4-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="b71d4-125">A ID de sub-rede da rede virtual para a regra.</span><span class="sxs-lookup"><span data-stu-id="b71d4-125">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="b71d4-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b71d4-126">-Confirm</span></span>
<span data-ttu-id="b71d4-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b71d4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b71d4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b71d4-128">-WhatIf</span></span>
<span data-ttu-id="b71d4-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b71d4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b71d4-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b71d4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b71d4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b71d4-131">CommonParameters</span></span>
<span data-ttu-id="b71d4-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b71d4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b71d4-133">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b71d4-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b71d4-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b71d4-134">INPUTS</span></span>

### <span data-ttu-id="b71d4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b71d4-135">System.String</span></span>

## <span data-ttu-id="b71d4-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b71d4-136">OUTPUTS</span></span>

### <span data-ttu-id="b71d4-137">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="b71d4-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="b71d4-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b71d4-138">NOTES</span></span>

## <span data-ttu-id="b71d4-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b71d4-139">RELATED LINKS</span></span>
