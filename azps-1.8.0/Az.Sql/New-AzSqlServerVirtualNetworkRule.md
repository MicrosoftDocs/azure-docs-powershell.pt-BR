---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 8667de4551e9fc0c4baf623099f70f778ec8f0a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598877"
---
# <span data-ttu-id="c688f-101">New-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c688f-101">New-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="c688f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c688f-102">SYNOPSIS</span></span>
<span data-ttu-id="c688f-103">Cria uma regra de rede virtual do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="c688f-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

## <span data-ttu-id="c688f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c688f-104">SYNTAX</span></span>

```
New-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c688f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c688f-105">DESCRIPTION</span></span>
<span data-ttu-id="c688f-106">Cria uma regra de rede virtual do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="c688f-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="c688f-107">As regras de rede virtual são usadas para conectar o SQL Server do Azure a uma rede virtual específica a fim de restringir o acesso no SQL Server do Azure apenas para estar disponível na rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c688f-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="c688f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c688f-108">EXAMPLES</span></span>

### <span data-ttu-id="c688f-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c688f-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="c688f-110">Cria uma regra de rede virtual do SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="c688f-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="c688f-111">OS</span><span class="sxs-lookup"><span data-stu-id="c688f-111">PARAMETERS</span></span>

### <span data-ttu-id="c688f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c688f-112">-AsJob</span></span>
<span data-ttu-id="c688f-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c688f-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c688f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c688f-114">-DefaultProfile</span></span>
<span data-ttu-id="c688f-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c688f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c688f-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c688f-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="c688f-117">Crie uma regra de firewall antes da rede virtual ter ponto de extremidade do serviço vnet habilitado.</span><span class="sxs-lookup"><span data-stu-id="c688f-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="c688f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c688f-118">-ResourceGroupName</span></span>
<span data-ttu-id="c688f-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c688f-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="c688f-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="c688f-120">-ServerName</span></span>
<span data-ttu-id="c688f-121">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="c688f-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="c688f-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="c688f-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="c688f-123">Nome da regra de rede virtual do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="c688f-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="c688f-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="c688f-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="c688f-125">A ID de sub-rede da rede virtual que especifica os detalhes da Microsoft. Network</span><span class="sxs-lookup"><span data-stu-id="c688f-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="c688f-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c688f-126">-Confirm</span></span>
<span data-ttu-id="c688f-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c688f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c688f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c688f-128">-WhatIf</span></span>
<span data-ttu-id="c688f-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c688f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c688f-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c688f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c688f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c688f-131">CommonParameters</span></span>
<span data-ttu-id="c688f-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c688f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c688f-133">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c688f-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c688f-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c688f-134">INPUTS</span></span>

### <span data-ttu-id="c688f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c688f-135">System.String</span></span>

## <span data-ttu-id="c688f-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c688f-136">OUTPUTS</span></span>

### <span data-ttu-id="c688f-137">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="c688f-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="c688f-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c688f-138">NOTES</span></span>

## <span data-ttu-id="c688f-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c688f-139">RELATED LINKS</span></span>
