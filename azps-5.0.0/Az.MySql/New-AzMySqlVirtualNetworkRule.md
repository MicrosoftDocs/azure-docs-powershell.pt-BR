---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 3b660f5db14e1197c1e262a10f8225e4e9a82b81
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118400"
---
# <span data-ttu-id="a39af-101">New-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a39af-101">New-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="a39af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a39af-102">SYNOPSIS</span></span>
<span data-ttu-id="a39af-103">Cria ou atualiza uma regra de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="a39af-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="a39af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a39af-104">SYNTAX</span></span>

```
New-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a39af-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a39af-105">DESCRIPTION</span></span>
<span data-ttu-id="a39af-106">Cria ou atualiza uma regra de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="a39af-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="a39af-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a39af-107">EXAMPLES</span></span>

### <span data-ttu-id="a39af-108">Exemplo 1: criar uma nova regra de rede virtual do servidor MySql</span><span class="sxs-lookup"><span data-stu-id="a39af-108">Example 1: Create a new MySql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> New-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="a39af-109">Esses cmdlets criam uma regra de rede virtual do MySql Server.</span><span class="sxs-lookup"><span data-stu-id="a39af-109">These cmdlets create a MySql server Virtual Network Rule.</span></span>

## <span data-ttu-id="a39af-110">OS</span><span class="sxs-lookup"><span data-stu-id="a39af-110">PARAMETERS</span></span>

### <span data-ttu-id="a39af-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a39af-111">-AsJob</span></span>
<span data-ttu-id="a39af-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="a39af-112">Run the command as a job</span></span>

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

### <span data-ttu-id="a39af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a39af-113">-DefaultProfile</span></span>
<span data-ttu-id="a39af-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a39af-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a39af-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a39af-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="a39af-116">Crie uma regra de firewall antes da rede virtual ter ponto de extremidade do serviço vnet habilitado.</span><span class="sxs-lookup"><span data-stu-id="a39af-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="a39af-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a39af-117">-Name</span></span>
<span data-ttu-id="a39af-118">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a39af-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="a39af-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a39af-119">-NoWait</span></span>
<span data-ttu-id="a39af-120">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="a39af-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a39af-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a39af-121">-PassThru</span></span>
<span data-ttu-id="a39af-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="a39af-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a39af-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a39af-123">-ResourceGroupName</span></span>
<span data-ttu-id="a39af-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a39af-124">The name of the resource group.</span></span>
<span data-ttu-id="a39af-125">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a39af-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a39af-126">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="a39af-126">-ServerName</span></span>
<span data-ttu-id="a39af-127">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="a39af-127">The name of the server.</span></span>

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

### <span data-ttu-id="a39af-128">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="a39af-128">-SubnetId</span></span>
<span data-ttu-id="a39af-129">A ID do recurso ARM da sub-rede da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a39af-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="a39af-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a39af-130">-SubscriptionId</span></span>
<span data-ttu-id="a39af-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a39af-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a39af-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a39af-132">-Confirm</span></span>
<span data-ttu-id="a39af-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a39af-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a39af-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a39af-134">-WhatIf</span></span>
<span data-ttu-id="a39af-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a39af-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a39af-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a39af-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a39af-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a39af-137">CommonParameters</span></span>
<span data-ttu-id="a39af-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a39af-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a39af-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a39af-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a39af-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a39af-140">INPUTS</span></span>

## <span data-ttu-id="a39af-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a39af-141">OUTPUTS</span></span>

### <span data-ttu-id="a39af-142">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a39af-142">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="a39af-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a39af-143">NOTES</span></span>

<span data-ttu-id="a39af-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a39af-144">ALIASES</span></span>

## <span data-ttu-id="a39af-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a39af-145">RELATED LINKS</span></span>

