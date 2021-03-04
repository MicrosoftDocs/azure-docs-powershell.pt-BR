---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/update-azsignalrnetworkacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
ms.openlocfilehash: 24552172c0f793c8414b5abfc9e6a66c747915d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885803"
---
# <span data-ttu-id="ed629-101">Update-AzSignalRNetworkAcl</span><span class="sxs-lookup"><span data-stu-id="ed629-101">Update-AzSignalRNetworkAcl</span></span>

## <span data-ttu-id="ed629-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed629-102">SYNOPSIS</span></span>
<span data-ttu-id="ed629-103">Atualize a ACL de rede de um serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="ed629-103">Update the Network ACL of a SignalR service.</span></span>

## <span data-ttu-id="ed629-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ed629-104">SYNTAX</span></span>

### <span data-ttu-id="ed629-105">ResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ed629-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalRNetworkAcl [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-DefaultAction <String>]
 [-PublicNetwork] [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed629-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed629-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -ResourceId <String> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed629-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed629-107">InputObjectParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -InputObject <PSSignalRResource> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed629-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ed629-108">DESCRIPTION</span></span>
<span data-ttu-id="ed629-109">Atualize a ACL de rede de um serviço SignalR, incluindo a ação padrão e as Acls de rede para conexão pública e privada.</span><span class="sxs-lookup"><span data-stu-id="ed629-109">Update the Network ACL of a SignalR service, including the default action and the network Acls for public and private connection.</span></span>

## <span data-ttu-id="ed629-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed629-110">EXAMPLES</span></span>

### <span data-ttu-id="ed629-111">Permitir RESTAPI,ClientConnection para rede pública e definir a ação padrão como Negar</span><span class="sxs-lookup"><span data-stu-id="ed629-111">Allow RESTAPI,ClientConnection for public network and set default action to Deny</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -DefaultAction Deny -PublicNetwork -Allow RESTAPI,ClientConnection

PS C:\>  $networkAcl

DefaultAction PublicNetwork                                        PrivateEndpoints
------------- -------------                                        ----------------
Deny          Microsoft.Azure.Commands.SignalR.Models.PSNetworkAcl {pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1}

PS C:\> $networkAcl.PublicNetwork
Allow                       Deny
-----                       ----
{ClientConnection, RESTAPI} {}
```

### <span data-ttu-id="ed629-112">Permitir conexão de cliente e conexão de servidor para uma conexão de ponto de extremidade privada</span><span class="sxs-lookup"><span data-stu-id="ed629-112">Allow client connection and server connection for a private endpoint connection</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -Allow ClientConnection,ServerConnection

PS C:\>$networkAcl.PrivateEndpoints[0]

Name                                           Allow                                Deny
----                                           -----                                ----
pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1 {ServerConnection, ClientConnection} {}
```

### <span data-ttu-id="ed629-113">Negar conexão de cliente para rede pública e uma conexão de ponto de extremidade privada</span><span class="sxs-lookup"><span data-stu-id="ed629-113">Deny client connection for both public network and a private endpoint connection</span></span>
```powershell
PS C:\>$networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -PublicNetwork -Deny ClientConnection
```

## <span data-ttu-id="ed629-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ed629-114">PARAMETERS</span></span>

### <span data-ttu-id="ed629-115">-Allow</span><span class="sxs-lookup"><span data-stu-id="ed629-115">-Allow</span></span>
<span data-ttu-id="ed629-116">ACLs de rede permitidas</span><span class="sxs-lookup"><span data-stu-id="ed629-116">Allowed network ACLs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ClientConnection, ServerConnection, RESTAPI

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed629-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed629-117">-AsJob</span></span>
<span data-ttu-id="ed629-118">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="ed629-118">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="ed629-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="ed629-119">-DefaultAction</span></span>
<span data-ttu-id="ed629-120">Ação padrão de ACLs de rede SignalR, permitir ou negar.</span><span class="sxs-lookup"><span data-stu-id="ed629-120">Default Action of SignalR network ACLs, either allow or deny.</span></span> <span data-ttu-id="ed629-121">Ele decide se as ACLs de rede ou permitem que ACLs de rede entre em vigor.</span><span class="sxs-lookup"><span data-stu-id="ed629-121">It decides whether deny network ACLs or allow network ACLs take effect.</span></span> <span data-ttu-id="ed629-122">Por exemplo, se a ação padrão for permitir, somente as ACLs de negação importam.</span><span class="sxs-lookup"><span data-stu-id="ed629-122">For example, if the default action is allow, then only the deny ACLs matters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed629-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed629-123">-DefaultProfile</span></span>
<span data-ttu-id="ed629-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed629-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed629-125">-Deny</span><span class="sxs-lookup"><span data-stu-id="ed629-125">-Deny</span></span>
<span data-ttu-id="ed629-126">ACLs de rede negadas</span><span class="sxs-lookup"><span data-stu-id="ed629-126">Denied network ACLs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ClientConnection, ServerConnection, RESTAPI

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed629-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed629-127">-InputObject</span></span>
<span data-ttu-id="ed629-128">O objeto de recurso SignalR.</span><span class="sxs-lookup"><span data-stu-id="ed629-128">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed629-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ed629-129">-Name</span></span>
<span data-ttu-id="ed629-130">O nome do serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="ed629-130">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed629-131">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="ed629-131">-PrivateEndpointName</span></span>
<span data-ttu-id="ed629-132">Name(s) of private endpoint(s) to be updated</span><span class="sxs-lookup"><span data-stu-id="ed629-132">Name(s) of private endpoint(s) to be updated</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed629-133">-PublicNetwork</span><span class="sxs-lookup"><span data-stu-id="ed629-133">-PublicNetwork</span></span>
<span data-ttu-id="ed629-134">Atualizar ACLs de rede pública</span><span class="sxs-lookup"><span data-stu-id="ed629-134">Update public network ACLs</span></span>

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

### <span data-ttu-id="ed629-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed629-135">-ResourceGroupName</span></span>
<span data-ttu-id="ed629-136">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed629-136">The resource group name.</span></span>
<span data-ttu-id="ed629-137">O padrão será usado se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="ed629-137">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed629-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed629-138">-ResourceId</span></span>
<span data-ttu-id="ed629-139">A ID do recurso de serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="ed629-139">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed629-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed629-140">-Confirm</span></span>
<span data-ttu-id="ed629-141">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed629-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed629-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed629-142">-WhatIf</span></span>
<span data-ttu-id="ed629-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ed629-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed629-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ed629-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed629-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed629-145">CommonParameters</span></span>
<span data-ttu-id="ed629-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed629-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed629-147">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed629-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed629-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed629-148">INPUTS</span></span>

### <span data-ttu-id="ed629-149">System.String</span><span class="sxs-lookup"><span data-stu-id="ed629-149">System.String</span></span>

## <span data-ttu-id="ed629-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ed629-150">OUTPUTS</span></span>

### <span data-ttu-id="ed629-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span><span class="sxs-lookup"><span data-stu-id="ed629-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span></span>

## <span data-ttu-id="ed629-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="ed629-152">NOTES</span></span>

## <span data-ttu-id="ed629-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed629-153">RELATED LINKS</span></span>
