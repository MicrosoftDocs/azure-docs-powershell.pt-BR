---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 5a29c0bbad712d99b03ab1ff5347cba5c07b02aa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272639"
---
# <span data-ttu-id="12605-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="12605-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="12605-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12605-102">SYNOPSIS</span></span>
<span data-ttu-id="12605-103">Cria um ponto de extremidade do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="12605-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="12605-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12605-104">SYNTAX</span></span>

### <span data-ttu-id="12605-105">AzureVM</span><span class="sxs-lookup"><span data-stu-id="12605-105">AzureVM</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVM] -ResourceId <String>
 [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12605-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="12605-106">AzureVNet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVNet] -ResourceId <String>
 [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12605-107">AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="12605-107">AzureSubnet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureSubnet] -ResourceId <String>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12605-108">ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="12605-108">ExternalAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-ExternalAddress] -Address <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12605-109">MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="12605-109">MMAWorkspaceMachine</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceMachine] -ResourceId <String>
 -Address <String> [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12605-110">MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="12605-110">MMAWorkspaceNetwork</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceNetwork] -ResourceId <String>
 -IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12605-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12605-111">DESCRIPTION</span></span>
<span data-ttu-id="12605-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet cria um ponto de extremidade de monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="12605-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="12605-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12605-113">EXAMPLES</span></span>

### <span data-ttu-id="12605-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="12605-114">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointScopeItem1 = New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndpointObject -Name "workspaceEndpoint" -MMAWorkspaceMachine -ResourceId $MySrcResourceId1 -IncludeItem $SrcEndpointScopeItem1
```

<span data-ttu-id="12605-115">Nome: workspaceEndpoint tipo: MMAWorkspaceMachine ResourceId:/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace endereço: Scope: {"include": [{"endereço": "WIN-P0HGNDO2S1B"}]}</span><span class="sxs-lookup"><span data-stu-id="12605-115">Name       : workspaceEndpoint Type       : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Scope     : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="12605-116">OS</span><span class="sxs-lookup"><span data-stu-id="12605-116">PARAMETERS</span></span>

### <span data-ttu-id="12605-117">-Endereço</span><span class="sxs-lookup"><span data-stu-id="12605-117">-Address</span></span>
<span data-ttu-id="12605-118">Endereço do ponto de extremidade do monitor de conexão (IP ou nome do domínio).</span><span class="sxs-lookup"><span data-stu-id="12605-118">Address of the connection monitor endpoint (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExternalAddress, MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12605-119">-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="12605-119">-AzureSubnet</span></span>
<span data-ttu-id="12605-120">Opção de ponto de extremidade de sub-rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="12605-120">Azure Subnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12605-121">-AzureVM</span><span class="sxs-lookup"><span data-stu-id="12605-121">-AzureVM</span></span>
<span data-ttu-id="12605-122">Comutador de ponto de extremidade da VM do Azure.</span><span class="sxs-lookup"><span data-stu-id="12605-122">Azure VM endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12605-123">-AzureVNet</span><span class="sxs-lookup"><span data-stu-id="12605-123">-AzureVNet</span></span>
<span data-ttu-id="12605-124">Comutador de ponto de extremidade da vnet do Azure.</span><span class="sxs-lookup"><span data-stu-id="12605-124">Azure Vnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVNet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12605-125">-CoverageLevel</span><span class="sxs-lookup"><span data-stu-id="12605-125">-CoverageLevel</span></span>
<span data-ttu-id="12605-126">Cobertura de teste para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="12605-126">Test coverage for the endpoint.</span></span>
<span data-ttu-id="12605-127">Os valores compatíveis são padrão, baixo, BelowAverage, média, AboveAvergae, completo.</span><span class="sxs-lookup"><span data-stu-id="12605-127">Supported values are Default, Low, BelowAverage, Average, AboveAvergae, Full.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12605-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12605-128">-DefaultProfile</span></span>
<span data-ttu-id="12605-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12605-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12605-130">-ExcludeItem</span><span class="sxs-lookup"><span data-stu-id="12605-130">-ExcludeItem</span></span>
<span data-ttu-id="12605-131">Lista de itens que precisam ser excluídos do escopo do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="12605-131">List of items which need to be excluded from endpoint scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12605-132">-ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="12605-132">-ExternalAddress</span></span>
<span data-ttu-id="12605-133">Chave de ponto de extremidade de endereço externo.</span><span class="sxs-lookup"><span data-stu-id="12605-133">External Address endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExternalAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12605-134">-IncludeItem</span><span class="sxs-lookup"><span data-stu-id="12605-134">-IncludeItem</span></span>
<span data-ttu-id="12605-135">Lista de itens que precisam ser incluídos no escopo endpont.</span><span class="sxs-lookup"><span data-stu-id="12605-135">List of items which need to be included into endpont scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, MMAWorkspaceMachine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12605-136">-MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="12605-136">-MMAWorkspaceMachine</span></span>
<span data-ttu-id="12605-137">Chave de ponto de extremidade da máquina do espaço de trabalho MMA</span><span class="sxs-lookup"><span data-stu-id="12605-137">MMA Workspace Machine endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12605-138">-MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="12605-138">-MMAWorkspaceNetwork</span></span>
<span data-ttu-id="12605-139">Chave de ponto de extremidade de rede do espaço de trabalho MMA</span><span class="sxs-lookup"><span data-stu-id="12605-139">MMA Workspace Network endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12605-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="12605-140">-Name</span></span>
<span data-ttu-id="12605-141">O nome do ponto de extremidade do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="12605-141">The name of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="12605-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12605-142">-ResourceId</span></span>
<span data-ttu-id="12605-143">ID do recurso do ponto de extremidade do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="12605-143">Resource ID of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM, AzureVNet, AzureSubnet, MMAWorkspaceMachine, MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12605-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="12605-144">-Confirm</span></span>
<span data-ttu-id="12605-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12605-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12605-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12605-146">-WhatIf</span></span>
<span data-ttu-id="12605-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="12605-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12605-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12605-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12605-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12605-149">CommonParameters</span></span>
<span data-ttu-id="12605-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12605-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12605-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12605-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12605-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12605-152">INPUTS</span></span>

### <span data-ttu-id="12605-153">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="12605-153">None</span></span>

## <span data-ttu-id="12605-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12605-154">OUTPUTS</span></span>

### <span data-ttu-id="12605-155">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="12605-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="12605-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12605-156">NOTES</span></span>

## <span data-ttu-id="12605-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12605-157">RELATED LINKS</span></span>
