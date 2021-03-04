---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/new-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: c6766e27c40f52b9d146590e91f6ecc73d5f32f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891012"
---
# <span data-ttu-id="3124c-101">New-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3124c-101">New-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="3124c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3124c-102">SYNOPSIS</span></span>
<span data-ttu-id="3124c-103">Cria ou atualiza uma regra de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="3124c-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="3124c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3124c-104">SYNTAX</span></span>

```
New-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3124c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3124c-105">DESCRIPTION</span></span>
<span data-ttu-id="3124c-106">Cria ou atualiza uma regra de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="3124c-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="3124c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3124c-107">EXAMPLES</span></span>

### <span data-ttu-id="3124c-108">Exemplo 1: Criar uma nova regra de rede virtual do servidor MySql</span><span class="sxs-lookup"><span data-stu-id="3124c-108">Example 1: Create a new MySql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> New-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="3124c-109">Esses cmdlets criam uma Regra de Rede Virtual do servidor MySql.</span><span class="sxs-lookup"><span data-stu-id="3124c-109">These cmdlets create a MySql server Virtual Network Rule.</span></span>

## <span data-ttu-id="3124c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3124c-110">PARAMETERS</span></span>

### <span data-ttu-id="3124c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3124c-111">-AsJob</span></span>
<span data-ttu-id="3124c-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="3124c-112">Run the command as a job</span></span>

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

### <span data-ttu-id="3124c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3124c-113">-DefaultProfile</span></span>
<span data-ttu-id="3124c-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3124c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3124c-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="3124c-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="3124c-116">Criar regra de firewall antes que a rede virtual tenha o ponto de extremidade do serviço vnet habilitado.</span><span class="sxs-lookup"><span data-stu-id="3124c-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="3124c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3124c-117">-Name</span></span>
<span data-ttu-id="3124c-118">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="3124c-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="3124c-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3124c-119">-NoWait</span></span>
<span data-ttu-id="3124c-120">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="3124c-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3124c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3124c-121">-PassThru</span></span>
<span data-ttu-id="3124c-122">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="3124c-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3124c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3124c-123">-ResourceGroupName</span></span>
<span data-ttu-id="3124c-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3124c-124">The name of the resource group.</span></span>
<span data-ttu-id="3124c-125">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3124c-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3124c-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3124c-126">-ServerName</span></span>
<span data-ttu-id="3124c-127">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="3124c-127">The name of the server.</span></span>

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

### <span data-ttu-id="3124c-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3124c-128">-SubnetId</span></span>
<span data-ttu-id="3124c-129">A ARM de recurso da sub-rede de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="3124c-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="3124c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3124c-130">-SubscriptionId</span></span>
<span data-ttu-id="3124c-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="3124c-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3124c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3124c-132">-Confirm</span></span>
<span data-ttu-id="3124c-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3124c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3124c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3124c-134">-WhatIf</span></span>
<span data-ttu-id="3124c-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3124c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3124c-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3124c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3124c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3124c-137">CommonParameters</span></span>
<span data-ttu-id="3124c-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3124c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3124c-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3124c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3124c-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3124c-140">INPUTS</span></span>

## <span data-ttu-id="3124c-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3124c-141">OUTPUTS</span></span>

### <span data-ttu-id="3124c-142">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3124c-142">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="3124c-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="3124c-143">NOTES</span></span>

<span data-ttu-id="3124c-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3124c-144">ALIASES</span></span>

## <span data-ttu-id="3124c-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3124c-145">RELATED LINKS</span></span>

