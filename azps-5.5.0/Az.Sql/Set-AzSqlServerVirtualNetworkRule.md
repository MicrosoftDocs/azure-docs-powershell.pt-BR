---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 55321b384a24e18a962b99cc40161eabbeb00160
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114462"
---
# <span data-ttu-id="677da-101">Set-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="677da-101">Set-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="677da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="677da-102">SYNOPSIS</span></span>
<span data-ttu-id="677da-103">Modifica a configuração de uma Regra de Rede Virtual do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="677da-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="677da-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="677da-104">SYNTAX</span></span>

```
Set-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="677da-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="677da-105">DESCRIPTION</span></span>
<span data-ttu-id="677da-106">Esse comando modifica a configuração de uma Regra de Rede Virtual do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="677da-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="677da-107">Para controlar o conjunto de regras de rede virtual no servidor, use 'Add-AzSqlServerVirtualNetworkRule' e 'Remove-AzSqlServerVirtualNetworkRule' em vez disso.</span><span class="sxs-lookup"><span data-stu-id="677da-107">To control the set of virtual network rules in the server, use 'Add-AzSqlServerVirtualNetworkRule' and 'Remove-AzSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="677da-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="677da-108">EXAMPLES</span></span>

### <span data-ttu-id="677da-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="677da-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="677da-110">Modifica uma regra de rede virtual existente com a nova ID da sub-rede virtual que contém informações sobre a nova rede virtual</span><span class="sxs-lookup"><span data-stu-id="677da-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="677da-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="677da-111">PARAMETERS</span></span>

### <span data-ttu-id="677da-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="677da-112">-AsJob</span></span>
<span data-ttu-id="677da-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="677da-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="677da-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="677da-114">-DefaultProfile</span></span>
<span data-ttu-id="677da-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="677da-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="677da-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="677da-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="677da-117">Crie uma regra de firewall antes que a rede virtual tenha o ponto de extremidade do serviço VNET habilitado.</span><span class="sxs-lookup"><span data-stu-id="677da-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="677da-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="677da-118">-ResourceGroupName</span></span>
<span data-ttu-id="677da-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="677da-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="677da-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="677da-120">-ServerName</span></span>
<span data-ttu-id="677da-121">O nome do Sql Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="677da-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="677da-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="677da-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="677da-123">O nome da Regra de Rede Virtual do Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="677da-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="677da-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="677da-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="677da-125">A ID da Sub-rede de Rede Virtual para a regra.</span><span class="sxs-lookup"><span data-stu-id="677da-125">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="677da-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="677da-126">-Confirm</span></span>
<span data-ttu-id="677da-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="677da-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="677da-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="677da-128">-WhatIf</span></span>
<span data-ttu-id="677da-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="677da-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="677da-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="677da-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="677da-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="677da-131">CommonParameters</span></span>
<span data-ttu-id="677da-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="677da-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="677da-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="677da-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="677da-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="677da-134">INPUTS</span></span>

### <span data-ttu-id="677da-135">System.String</span><span class="sxs-lookup"><span data-stu-id="677da-135">System.String</span></span>

## <span data-ttu-id="677da-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="677da-136">OUTPUTS</span></span>

### <span data-ttu-id="677da-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="677da-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="677da-138">Notas</span><span class="sxs-lookup"><span data-stu-id="677da-138">NOTES</span></span>

## <span data-ttu-id="677da-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="677da-139">RELATED LINKS</span></span>
