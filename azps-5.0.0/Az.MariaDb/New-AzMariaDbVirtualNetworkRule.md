---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 77a89dec96e0e9b7ca7bd003f8368274edf6acdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124586"
---
# <span data-ttu-id="f969c-101">New-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f969c-101">New-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="f969c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f969c-102">SYNOPSIS</span></span>
<span data-ttu-id="f969c-103">Cria ou atualiza uma regra de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="f969c-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="f969c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f969c-104">SYNTAX</span></span>

```
New-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f969c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f969c-105">DESCRIPTION</span></span>
<span data-ttu-id="f969c-106">Cria ou atualiza uma regra de rede virtual existente.</span><span class="sxs-lookup"><span data-stu-id="f969c-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="f969c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f969c-107">EXAMPLES</span></span>

### <span data-ttu-id="f969c-108">Exemplo 1: criar uma regra de rede virtual para um MariaDB</span><span class="sxs-lookup"><span data-stu-id="f969c-108">Example 1: Create a virtual network rule for a MariaDB</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> New-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnet-001 -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name     Type
----     ----
vnet-001 Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="f969c-109">Esse comando cria uma regra de rede virtual para um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="f969c-109">This command creates a virtual network rule for a MariaDB.</span></span>

## <span data-ttu-id="f969c-110">OS</span><span class="sxs-lookup"><span data-stu-id="f969c-110">PARAMETERS</span></span>

### <span data-ttu-id="f969c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f969c-111">-AsJob</span></span>
<span data-ttu-id="f969c-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="f969c-112">Run the command as a job</span></span>

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

### <span data-ttu-id="f969c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f969c-113">-DefaultProfile</span></span>
<span data-ttu-id="f969c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f969c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f969c-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f969c-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="f969c-116">Crie uma regra de firewall antes da rede virtual ter ponto de extremidade do serviço vnet habilitado.</span><span class="sxs-lookup"><span data-stu-id="f969c-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="f969c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f969c-117">-Name</span></span>
<span data-ttu-id="f969c-118">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f969c-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="f969c-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f969c-119">-NoWait</span></span>
<span data-ttu-id="f969c-120">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="f969c-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f969c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f969c-121">-PassThru</span></span>
<span data-ttu-id="f969c-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="f969c-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f969c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f969c-123">-ResourceGroupName</span></span>
<span data-ttu-id="f969c-124">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="f969c-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f969c-125">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="f969c-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f969c-126">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f969c-126">-ServerName</span></span>
<span data-ttu-id="f969c-127">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="f969c-127">The name of the server.</span></span>

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

### <span data-ttu-id="f969c-128">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="f969c-128">-SubnetId</span></span>
<span data-ttu-id="f969c-129">A ID do recurso ARM da sub-rede da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f969c-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="f969c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f969c-130">-SubscriptionId</span></span>
<span data-ttu-id="f969c-131">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="f969c-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="f969c-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f969c-132">-Confirm</span></span>
<span data-ttu-id="f969c-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f969c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f969c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f969c-134">-WhatIf</span></span>
<span data-ttu-id="f969c-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f969c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f969c-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f969c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f969c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f969c-137">CommonParameters</span></span>
<span data-ttu-id="f969c-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f969c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f969c-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f969c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f969c-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f969c-140">INPUTS</span></span>

## <span data-ttu-id="f969c-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f969c-141">OUTPUTS</span></span>

### <span data-ttu-id="f969c-142">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. Api20180601Preview. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f969c-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="f969c-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f969c-143">NOTES</span></span>

<span data-ttu-id="f969c-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f969c-144">ALIASES</span></span>

## <span data-ttu-id="f969c-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f969c-145">RELATED LINKS</span></span>

