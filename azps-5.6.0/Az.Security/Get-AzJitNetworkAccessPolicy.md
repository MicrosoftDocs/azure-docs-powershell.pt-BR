---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 980b680130ca319612bbbf28e787ebd99c4bf8bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887951"
---
# <span data-ttu-id="aa860-101">Get-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aa860-101">Get-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="aa860-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa860-102">SYNOPSIS</span></span>
<span data-ttu-id="aa860-103">Obtém as políticas de acesso à rede JIT</span><span class="sxs-lookup"><span data-stu-id="aa860-103">Gets the JIT network access policies</span></span>

## <span data-ttu-id="aa860-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="aa860-104">SYNTAX</span></span>

### <span data-ttu-id="aa860-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="aa860-105">SubscriptionScope (Default)</span></span>
```
Get-AzJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa860-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="aa860-106">ResourceGroupScope</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aa860-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="aa860-107">ResourceGroupLevelResource</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa860-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa860-108">ResourceId</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa860-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="aa860-109">DESCRIPTION</span></span>
<span data-ttu-id="aa860-110">As políticas de acesso à rede Just In Time (JIT) permitem definir uma política que permitirá que usuários simples criem uma conexão de rede temporária com uma VM.</span><span class="sxs-lookup"><span data-stu-id="aa860-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="aa860-111">A política define quais portas, protocolo e endereços IP de origem podem solicitar uma conexão com uma VM e a duração máxima antes que a conexão seja fechada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="aa860-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="aa860-112">Na política, você também pode ver a solicitação de conexão que foi feita com essa política.</span><span class="sxs-lookup"><span data-stu-id="aa860-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="aa860-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa860-113">EXAMPLES</span></span>

### <span data-ttu-id="aa860-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aa860-114">Example 1</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/northeurope/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="aa860-115">Obter todas as polícias de acesso à rede JIT em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="aa860-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="aa860-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="aa860-116">Example 2</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/northeurope/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="aa860-117">Obter todas as polícias de acesso à rede JIT no grupo de recursos "myService1"</span><span class="sxs-lookup"><span data-stu-id="aa860-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="aa860-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="aa860-118">Example 3</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="aa860-119">Obtém uma política de acesso de rede JIT específica</span><span class="sxs-lookup"><span data-stu-id="aa860-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="aa860-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="aa860-120">PARAMETERS</span></span>

### <span data-ttu-id="aa860-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa860-121">-DefaultProfile</span></span>
<span data-ttu-id="aa860-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aa860-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa860-123">-Location</span><span class="sxs-lookup"><span data-stu-id="aa860-123">-Location</span></span>
<span data-ttu-id="aa860-124">Local.</span><span class="sxs-lookup"><span data-stu-id="aa860-124">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa860-125">-Name</span><span class="sxs-lookup"><span data-stu-id="aa860-125">-Name</span></span>
<span data-ttu-id="aa860-126">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="aa860-126">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa860-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa860-127">-ResourceGroupName</span></span>
<span data-ttu-id="aa860-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aa860-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa860-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa860-129">-ResourceId</span></span>
<span data-ttu-id="aa860-130">A id de recurso do recurso jit Network Access Policy.</span><span class="sxs-lookup"><span data-stu-id="aa860-130">The resource id of the jit Network Access Policy resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa860-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa860-131">CommonParameters</span></span>
<span data-ttu-id="aa860-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa860-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa860-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa860-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa860-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa860-134">INPUTS</span></span>

### <span data-ttu-id="aa860-135">System.String</span><span class="sxs-lookup"><span data-stu-id="aa860-135">System.String</span></span>

## <span data-ttu-id="aa860-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="aa860-136">OUTPUTS</span></span>

### <span data-ttu-id="aa860-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aa860-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="aa860-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="aa860-138">NOTES</span></span>

## <span data-ttu-id="aa860-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa860-139">RELATED LINKS</span></span>
