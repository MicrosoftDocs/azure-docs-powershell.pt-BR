---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: c2e3386d7c9146eeaa96220ddcbea4cf50864e10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427136"
---
# <span data-ttu-id="c69a5-101">New-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c69a5-101">New-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="c69a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c69a5-102">SYNOPSIS</span></span>
<span data-ttu-id="c69a5-103">Cria uma regra de rede virtual do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="c69a5-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c69a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c69a5-104">SYNTAX</span></span>

```
New-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c69a5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c69a5-105">DESCRIPTION</span></span>
<span data-ttu-id="c69a5-106">Cria uma regra de rede virtual do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="c69a5-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="c69a5-107">As regras de rede virtual são usadas para conectar o SQL Server do Azure a uma rede virtual específica a fim de restringir o acesso no SQL Server do Azure apenas para estar disponível na rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c69a5-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="c69a5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c69a5-108">EXAMPLES</span></span>

### <span data-ttu-id="c69a5-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c69a5-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="c69a5-110">Cria uma regra de rede virtual do SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="c69a5-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="c69a5-111">OS</span><span class="sxs-lookup"><span data-stu-id="c69a5-111">PARAMETERS</span></span>

### <span data-ttu-id="c69a5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c69a5-112">-AsJob</span></span>
<span data-ttu-id="c69a5-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c69a5-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c69a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c69a5-114">-DefaultProfile</span></span>
<span data-ttu-id="c69a5-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c69a5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c69a5-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c69a5-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="c69a5-117">Crie uma regra de firewall antes da rede virtual ter ponto de extremidade do serviço vnet habilitado.</span><span class="sxs-lookup"><span data-stu-id="c69a5-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="c69a5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c69a5-118">-ResourceGroupName</span></span>
<span data-ttu-id="c69a5-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c69a5-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="c69a5-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="c69a5-120">-ServerName</span></span>
<span data-ttu-id="c69a5-121">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="c69a5-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="c69a5-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="c69a5-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="c69a5-123">Nome da regra de rede virtual do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="c69a5-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="c69a5-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="c69a5-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="c69a5-125">A ID de sub-rede da rede virtual que especifica os detalhes da Microsoft. Network</span><span class="sxs-lookup"><span data-stu-id="c69a5-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="c69a5-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c69a5-126">-Confirm</span></span>
<span data-ttu-id="c69a5-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c69a5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c69a5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c69a5-128">-WhatIf</span></span>
<span data-ttu-id="c69a5-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c69a5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c69a5-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c69a5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c69a5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c69a5-131">CommonParameters</span></span>
<span data-ttu-id="c69a5-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c69a5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c69a5-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c69a5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c69a5-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c69a5-134">INPUTS</span></span>

### <span data-ttu-id="c69a5-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c69a5-135">System.String</span></span>

## <span data-ttu-id="c69a5-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c69a5-136">OUTPUTS</span></span>

### <span data-ttu-id="c69a5-137">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="c69a5-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="c69a5-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c69a5-138">NOTES</span></span>

## <span data-ttu-id="c69a5-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c69a5-139">RELATED LINKS</span></span>
