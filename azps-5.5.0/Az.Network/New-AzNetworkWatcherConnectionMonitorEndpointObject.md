---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 5a29c0bbad712d99b03ab1ff5347cba5c07b02aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118308"
---
# <span data-ttu-id="fea83-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="fea83-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="fea83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fea83-102">SYNOPSIS</span></span>
<span data-ttu-id="fea83-103">Cria o ponto de extremidade do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="fea83-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="fea83-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fea83-104">SYNTAX</span></span>

### <span data-ttu-id="fea83-105">AzureVM</span><span class="sxs-lookup"><span data-stu-id="fea83-105">AzureVM</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVM] -ResourceId <String>
 [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fea83-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="fea83-106">AzureVNet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVNet] -ResourceId <String>
 [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fea83-107">AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="fea83-107">AzureSubnet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureSubnet] -ResourceId <String>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fea83-108">Externaladdress</span><span class="sxs-lookup"><span data-stu-id="fea83-108">ExternalAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-ExternalAddress] -Address <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fea83-109">MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="fea83-109">MMAWorkspaceMachine</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceMachine] -ResourceId <String>
 -Address <String> [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fea83-110">MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="fea83-110">MMAWorkspaceNetwork</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceNetwork] -ResourceId <String>
 -IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fea83-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="fea83-111">DESCRIPTION</span></span>
<span data-ttu-id="fea83-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet cria o ponto de extremidade do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="fea83-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="fea83-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fea83-113">EXAMPLES</span></span>

### <span data-ttu-id="fea83-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fea83-114">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointScopeItem1 = New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndpointObject -Name "workspaceEndpoint" -MMAWorkspaceMachine -ResourceId $MySrcResourceId1 -IncludeItem $SrcEndpointScopeItem1
```

<span data-ttu-id="fea83-115">Nome: tipo de ponto de trabalhoEndpoint: MMAWorkspaceMachine ResourceId: /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address: Scope: { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] } }</span><span class="sxs-lookup"><span data-stu-id="fea83-115">Name       : workspaceEndpoint Type       : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Scope     : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="fea83-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fea83-116">PARAMETERS</span></span>

### <span data-ttu-id="fea83-117">-Endereço</span><span class="sxs-lookup"><span data-stu-id="fea83-117">-Address</span></span>
<span data-ttu-id="fea83-118">Endereço do ponto de extremidade do monitor de conexão (IP ou nome de domínio).</span><span class="sxs-lookup"><span data-stu-id="fea83-118">Address of the connection monitor endpoint (IP or domain name).</span></span>

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

### <span data-ttu-id="fea83-119">-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="fea83-119">-AzureSubnet</span></span>
<span data-ttu-id="fea83-120">Opção de ponto de extremidade da Sub-rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="fea83-120">Azure Subnet endpoint switch.</span></span>

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

### <span data-ttu-id="fea83-121">-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fea83-121">-AzureVM</span></span>
<span data-ttu-id="fea83-122">Opção de ponto de extremidade VM do Azure.</span><span class="sxs-lookup"><span data-stu-id="fea83-122">Azure VM endpoint switch.</span></span>

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

### <span data-ttu-id="fea83-123">-AzureVNet</span><span class="sxs-lookup"><span data-stu-id="fea83-123">-AzureVNet</span></span>
<span data-ttu-id="fea83-124">Opção de ponto de extremidade do Azure Vnet.</span><span class="sxs-lookup"><span data-stu-id="fea83-124">Azure Vnet endpoint switch.</span></span>

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

### <span data-ttu-id="fea83-125">-CoverageLevel</span><span class="sxs-lookup"><span data-stu-id="fea83-125">-CoverageLevel</span></span>
<span data-ttu-id="fea83-126">Cobertura de teste para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="fea83-126">Test coverage for the endpoint.</span></span>
<span data-ttu-id="fea83-127">Os valores com suporte são Padrão, Baixo, Abaixo de Média, Média, Acima deAvergae, Completo.</span><span class="sxs-lookup"><span data-stu-id="fea83-127">Supported values are Default, Low, BelowAverage, Average, AboveAvergae, Full.</span></span>

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

### <span data-ttu-id="fea83-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fea83-128">-DefaultProfile</span></span>
<span data-ttu-id="fea83-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fea83-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fea83-130">-ExcludeItem</span><span class="sxs-lookup"><span data-stu-id="fea83-130">-ExcludeItem</span></span>
<span data-ttu-id="fea83-131">Lista de itens que precisam ser excluídos do escopo do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="fea83-131">List of items which need to be excluded from endpoint scope.</span></span>

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

### <span data-ttu-id="fea83-132">-ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="fea83-132">-ExternalAddress</span></span>
<span data-ttu-id="fea83-133">Opção do ponto de extremidade endereço externo.</span><span class="sxs-lookup"><span data-stu-id="fea83-133">External Address endpoint switch.</span></span>

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

### <span data-ttu-id="fea83-134">-IncludeItem</span><span class="sxs-lookup"><span data-stu-id="fea83-134">-IncludeItem</span></span>
<span data-ttu-id="fea83-135">Lista de itens que precisam ser incluídos no escopo de endpont.</span><span class="sxs-lookup"><span data-stu-id="fea83-135">List of items which need to be included into endpont scope.</span></span>

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

### <span data-ttu-id="fea83-136">-MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="fea83-136">-MMAWorkspaceMachine</span></span>
<span data-ttu-id="fea83-137">Opção de ponto de extremidade MMA Workspace Machine.</span><span class="sxs-lookup"><span data-stu-id="fea83-137">MMA Workspace Machine endpoint switch.</span></span>

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

### <span data-ttu-id="fea83-138">-MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="fea83-138">-MMAWorkspaceNetwork</span></span>
<span data-ttu-id="fea83-139">Opção de ponto de extremidade MMA Workspace Network.</span><span class="sxs-lookup"><span data-stu-id="fea83-139">MMA Workspace Network endpoint switch.</span></span>

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

### <span data-ttu-id="fea83-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="fea83-140">-Name</span></span>
<span data-ttu-id="fea83-141">O nome do ponto de extremidade do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="fea83-141">The name of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="fea83-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fea83-142">-ResourceId</span></span>
<span data-ttu-id="fea83-143">ID do recurso do ponto de extremidade do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="fea83-143">Resource ID of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="fea83-144">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fea83-144">-Confirm</span></span>
<span data-ttu-id="fea83-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fea83-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fea83-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fea83-146">-WhatIf</span></span>
<span data-ttu-id="fea83-147">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fea83-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fea83-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fea83-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fea83-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea83-149">CommonParameters</span></span>
<span data-ttu-id="fea83-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fea83-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea83-151">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fea83-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea83-152">Entradas</span><span class="sxs-lookup"><span data-stu-id="fea83-152">INPUTS</span></span>

### <span data-ttu-id="fea83-153">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fea83-153">None</span></span>

## <span data-ttu-id="fea83-154">Saídas</span><span class="sxs-lookup"><span data-stu-id="fea83-154">OUTPUTS</span></span>

### <span data-ttu-id="fea83-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="fea83-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="fea83-156">Notas</span><span class="sxs-lookup"><span data-stu-id="fea83-156">NOTES</span></span>

## <span data-ttu-id="fea83-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fea83-157">RELATED LINKS</span></span>
