---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalrnetworkacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
ms.openlocfilehash: afe9e1f604754c88035ed79f0eb480321ca348ba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432998"
---
# <span data-ttu-id="4d85c-101">Update-AzSignalRNetworkAcl</span><span class="sxs-lookup"><span data-stu-id="4d85c-101">Update-AzSignalRNetworkAcl</span></span>

## <span data-ttu-id="4d85c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d85c-102">SYNOPSIS</span></span>
<span data-ttu-id="4d85c-103">Atualize a ACL de rede de um serviço de sinal de acesso.</span><span class="sxs-lookup"><span data-stu-id="4d85c-103">Update the Network ACL of a SignalR service.</span></span>

## <span data-ttu-id="4d85c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d85c-104">SYNTAX</span></span>

### <span data-ttu-id="4d85c-105">ResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4d85c-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalRNetworkAcl [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-DefaultAction <String>]
 [-PublicNetwork] [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d85c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d85c-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -ResourceId <String> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d85c-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d85c-107">InputObjectParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -InputObject <PSSignalRResource> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d85c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4d85c-108">DESCRIPTION</span></span>
<span data-ttu-id="4d85c-109">Atualize a ACL de rede de um serviço de sinal, incluindo a ação padrão e as ACLs de rede para conexão pública e privada.</span><span class="sxs-lookup"><span data-stu-id="4d85c-109">Update the Network ACL of a SignalR service, including the default action and the network Acls for public and private connection.</span></span>

## <span data-ttu-id="4d85c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4d85c-110">EXAMPLES</span></span>

### <span data-ttu-id="4d85c-111">Permitir o RESTAPI, o ClientConnection para redes públicas e definir a ação padrão para recusar</span><span class="sxs-lookup"><span data-stu-id="4d85c-111">Allow RESTAPI,ClientConnection for public network and set default action to Deny</span></span>
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

### <span data-ttu-id="4d85c-112">Permitir conexão do cliente e conexão do servidor para uma conexão de ponto de extremidade particular</span><span class="sxs-lookup"><span data-stu-id="4d85c-112">Allow client connection and server connection for a private endpoint connection</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -Allow ClientConnection,ServerConnection

PS C:\>$networkAcl.PrivateEndpoints[0]

Name                                           Allow                                Deny
----                                           -----                                ----
pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1 {ServerConnection, ClientConnection} {}
```

### <span data-ttu-id="4d85c-113">Negar conexão do cliente para a rede pública e uma conexão de ponto de extremidade particular</span><span class="sxs-lookup"><span data-stu-id="4d85c-113">Deny client connection for both public network and a private endpoint connection</span></span>
```powershell
PS C:\>$networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -PublicNetwork -Deny ClientConnection
```

## <span data-ttu-id="4d85c-114">OS</span><span class="sxs-lookup"><span data-stu-id="4d85c-114">PARAMETERS</span></span>

### <span data-ttu-id="4d85c-115">-Permitir</span><span class="sxs-lookup"><span data-stu-id="4d85c-115">-Allow</span></span>
<span data-ttu-id="4d85c-116">ACLs de rede permitidas</span><span class="sxs-lookup"><span data-stu-id="4d85c-116">Allowed network ACLs</span></span>

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

### <span data-ttu-id="4d85c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d85c-117">-AsJob</span></span>
<span data-ttu-id="4d85c-118">Execute o cmdlet em plano de trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="4d85c-118">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="4d85c-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="4d85c-119">-DefaultAction</span></span>
<span data-ttu-id="4d85c-120">A ação padrão das ACLs de rede Signalr, permitir ou recusar.</span><span class="sxs-lookup"><span data-stu-id="4d85c-120">Default Action of SignalR network ACLs, either allow or deny.</span></span> <span data-ttu-id="4d85c-121">Ele decide se a negação de ACLs de rede ou permite que ACLs de rede entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="4d85c-121">It decides whether deny network ACLs or allow network ACLs take effect.</span></span> <span data-ttu-id="4d85c-122">Por exemplo, se a ação padrão for permitir, somente as ACLs de negação serão importantes.</span><span class="sxs-lookup"><span data-stu-id="4d85c-122">For example, if the default action is allow, then only the deny ACLs matters.</span></span>

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

### <span data-ttu-id="4d85c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d85c-123">-DefaultProfile</span></span>
<span data-ttu-id="4d85c-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4d85c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d85c-125">-Negar</span><span class="sxs-lookup"><span data-stu-id="4d85c-125">-Deny</span></span>
<span data-ttu-id="4d85c-126">ACLs de rede negadas</span><span class="sxs-lookup"><span data-stu-id="4d85c-126">Denied network ACLs</span></span>

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

### <span data-ttu-id="4d85c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d85c-127">-InputObject</span></span>
<span data-ttu-id="4d85c-128">O objeto de recurso Signalr.</span><span class="sxs-lookup"><span data-stu-id="4d85c-128">The SignalR resource object.</span></span>

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

### <span data-ttu-id="4d85c-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d85c-129">-Name</span></span>
<span data-ttu-id="4d85c-130">O nome do serviço do Signalr.</span><span class="sxs-lookup"><span data-stu-id="4d85c-130">The SignalR service name.</span></span>

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

### <span data-ttu-id="4d85c-131">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="4d85c-131">-PrivateEndpointName</span></span>
<span data-ttu-id="4d85c-132">Nome (s) de ponto (s) particular (is) a ser atualizado (s)</span><span class="sxs-lookup"><span data-stu-id="4d85c-132">Name(s) of private endpoint(s) to be updated</span></span>

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

### <span data-ttu-id="4d85c-133">-PublicNetwork</span><span class="sxs-lookup"><span data-stu-id="4d85c-133">-PublicNetwork</span></span>
<span data-ttu-id="4d85c-134">Atualizar ACLs de rede pública</span><span class="sxs-lookup"><span data-stu-id="4d85c-134">Update public network ACLs</span></span>

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

### <span data-ttu-id="4d85c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d85c-135">-ResourceGroupName</span></span>
<span data-ttu-id="4d85c-136">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d85c-136">The resource group name.</span></span>
<span data-ttu-id="4d85c-137">O padrão será usado se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="4d85c-137">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="4d85c-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d85c-138">-ResourceId</span></span>
<span data-ttu-id="4d85c-139">A ID de recurso do serviço Signalr.</span><span class="sxs-lookup"><span data-stu-id="4d85c-139">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="4d85c-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4d85c-140">-Confirm</span></span>
<span data-ttu-id="4d85c-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d85c-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d85c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d85c-142">-WhatIf</span></span>
<span data-ttu-id="4d85c-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4d85c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d85c-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4d85c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d85c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d85c-145">CommonParameters</span></span>
<span data-ttu-id="4d85c-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d85c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d85c-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d85c-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d85c-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4d85c-148">INPUTS</span></span>

### <span data-ttu-id="4d85c-149">System. String</span><span class="sxs-lookup"><span data-stu-id="4d85c-149">System.String</span></span>

## <span data-ttu-id="4d85c-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4d85c-150">OUTPUTS</span></span>

### <span data-ttu-id="4d85c-151">Microsoft. Azure. Commands. Signalr. Models. PSSignalRNetworkAcls</span><span class="sxs-lookup"><span data-stu-id="4d85c-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span></span>

## <span data-ttu-id="4d85c-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4d85c-152">NOTES</span></span>

## <span data-ttu-id="4d85c-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d85c-153">RELATED LINKS</span></span>
