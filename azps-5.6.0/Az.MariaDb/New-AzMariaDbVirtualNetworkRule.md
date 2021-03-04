---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/new-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: cfbbfd9472d18d75dea3da68cb4d2e06cf54c9a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887707"
---
# <span data-ttu-id="721f8-101">New-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="721f8-101">New-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="721f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="721f8-102">SYNOPSIS</span></span>
<span data-ttu-id="721f8-103">Cria ou atualiza uma regra de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="721f8-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="721f8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="721f8-104">SYNTAX</span></span>

```
New-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="721f8-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="721f8-105">DESCRIPTION</span></span>
<span data-ttu-id="721f8-106">Cria ou atualiza uma regra de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="721f8-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="721f8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="721f8-107">EXAMPLES</span></span>

### <span data-ttu-id="721f8-108">Exemplo 1: Criar uma regra de rede virtual para um MariaDB</span><span class="sxs-lookup"><span data-stu-id="721f8-108">Example 1: Create a virtual network rule for a MariaDB</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> New-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnet-001 -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name     Type
----     ----
vnet-001 Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="721f8-109">Este comando cria uma regra de rede virtual para um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="721f8-109">This command creates a virtual network rule for a MariaDB.</span></span>

## <span data-ttu-id="721f8-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="721f8-110">PARAMETERS</span></span>

### <span data-ttu-id="721f8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="721f8-111">-AsJob</span></span>
<span data-ttu-id="721f8-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="721f8-112">Run the command as a job</span></span>

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

### <span data-ttu-id="721f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="721f8-113">-DefaultProfile</span></span>
<span data-ttu-id="721f8-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="721f8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="721f8-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="721f8-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="721f8-116">Criar regra de firewall antes que a rede virtual tenha o ponto de extremidade do serviço vnet habilitado.</span><span class="sxs-lookup"><span data-stu-id="721f8-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="721f8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="721f8-117">-Name</span></span>
<span data-ttu-id="721f8-118">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="721f8-118">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="721f8-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="721f8-119">-NoWait</span></span>
<span data-ttu-id="721f8-120">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="721f8-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="721f8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="721f8-121">-PassThru</span></span>
<span data-ttu-id="721f8-122">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="721f8-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="721f8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="721f8-123">-ResourceGroupName</span></span>
<span data-ttu-id="721f8-124">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="721f8-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="721f8-125">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="721f8-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="721f8-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="721f8-126">-ServerName</span></span>
<span data-ttu-id="721f8-127">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="721f8-127">The name of the server.</span></span>

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

### <span data-ttu-id="721f8-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="721f8-128">-SubnetId</span></span>
<span data-ttu-id="721f8-129">A ARM de recurso da sub-rede de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="721f8-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="721f8-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="721f8-130">-SubscriptionId</span></span>
<span data-ttu-id="721f8-131">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="721f8-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="721f8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="721f8-132">-Confirm</span></span>
<span data-ttu-id="721f8-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="721f8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="721f8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="721f8-134">-WhatIf</span></span>
<span data-ttu-id="721f8-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="721f8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="721f8-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="721f8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="721f8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="721f8-137">CommonParameters</span></span>
<span data-ttu-id="721f8-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="721f8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="721f8-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="721f8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="721f8-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="721f8-140">INPUTS</span></span>

## <span data-ttu-id="721f8-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="721f8-141">OUTPUTS</span></span>

### <span data-ttu-id="721f8-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="721f8-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="721f8-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="721f8-143">NOTES</span></span>

<span data-ttu-id="721f8-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="721f8-144">ALIASES</span></span>

## <span data-ttu-id="721f8-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="721f8-145">RELATED LINKS</span></span>

