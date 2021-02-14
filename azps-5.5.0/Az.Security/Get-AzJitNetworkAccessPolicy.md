---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: e82c540b946408671c424a1f86d3266a7e6d6906
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110801"
---
# <span data-ttu-id="ace24-101">Get-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ace24-101">Get-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="ace24-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ace24-102">SYNOPSIS</span></span>
<span data-ttu-id="ace24-103">Obtém as políticas de acesso à rede JIT</span><span class="sxs-lookup"><span data-stu-id="ace24-103">Gets the JIT network access policies</span></span>

## <span data-ttu-id="ace24-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ace24-104">SYNTAX</span></span>

### <span data-ttu-id="ace24-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ace24-105">SubscriptionScope (Default)</span></span>
```
Get-AzJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ace24-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="ace24-106">ResourceGroupScope</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ace24-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="ace24-107">ResourceGroupLevelResource</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ace24-108">Resourceid</span><span class="sxs-lookup"><span data-stu-id="ace24-108">ResourceId</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ace24-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ace24-109">DESCRIPTION</span></span>
<span data-ttu-id="ace24-110">As políticas de acesso à rede Just In Time (JIT) permitem que você defina uma política para permitir que usuários simples criem uma conexão de rede temporária com um VM.</span><span class="sxs-lookup"><span data-stu-id="ace24-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="ace24-111">A política define quais portas, protocolo e endereços IP de origem podem solicitar uma conexão com um VM e a duração máxima antes que a conexão seja fechada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ace24-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="ace24-112">Na política, você também pode ver a solicitação de conexão que foi feita com essa política.</span><span class="sxs-lookup"><span data-stu-id="ace24-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="ace24-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ace24-113">EXAMPLES</span></span>

### <span data-ttu-id="ace24-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ace24-114">Example 1</span></span>
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

<span data-ttu-id="ace24-115">Obter todas as equipes de acesso à rede JIT em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="ace24-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="ace24-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ace24-116">Example 2</span></span>
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

<span data-ttu-id="ace24-117">Obter todas as equipes de acesso à rede JIT no grupo de recursos "meuService1"</span><span class="sxs-lookup"><span data-stu-id="ace24-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="ace24-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ace24-118">Example 3</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="ace24-119">Obtém uma política de acesso de rede JIT específica</span><span class="sxs-lookup"><span data-stu-id="ace24-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="ace24-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ace24-120">PARAMETERS</span></span>

### <span data-ttu-id="ace24-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ace24-121">-DefaultProfile</span></span>
<span data-ttu-id="ace24-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ace24-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ace24-123">-Local</span><span class="sxs-lookup"><span data-stu-id="ace24-123">-Location</span></span>
<span data-ttu-id="ace24-124">Localização.</span><span class="sxs-lookup"><span data-stu-id="ace24-124">Location.</span></span>

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

### <span data-ttu-id="ace24-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="ace24-125">-Name</span></span>
<span data-ttu-id="ace24-126">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ace24-126">Resource name.</span></span>

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

### <span data-ttu-id="ace24-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ace24-127">-ResourceGroupName</span></span>
<span data-ttu-id="ace24-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ace24-128">Resource group name.</span></span>

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

### <span data-ttu-id="ace24-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ace24-129">-ResourceId</span></span>
<span data-ttu-id="ace24-130">A ID do recurso jit Network Access Policy.</span><span class="sxs-lookup"><span data-stu-id="ace24-130">The resource id of the jit Network Access Policy resource.</span></span>

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

### <span data-ttu-id="ace24-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ace24-131">CommonParameters</span></span>
<span data-ttu-id="ace24-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ace24-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ace24-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ace24-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ace24-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="ace24-134">INPUTS</span></span>

### <span data-ttu-id="ace24-135">System.String</span><span class="sxs-lookup"><span data-stu-id="ace24-135">System.String</span></span>

## <span data-ttu-id="ace24-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="ace24-136">OUTPUTS</span></span>

### <span data-ttu-id="ace24-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ace24-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="ace24-138">Notas</span><span class="sxs-lookup"><span data-stu-id="ace24-138">NOTES</span></span>

## <span data-ttu-id="ace24-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ace24-139">RELATED LINKS</span></span>
