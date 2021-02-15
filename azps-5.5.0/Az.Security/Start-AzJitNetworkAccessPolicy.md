---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 0efde69aec3b30c58aee8c42aeb1703215219c2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118685"
---
# <span data-ttu-id="a79b9-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a79b9-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="a79b9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a79b9-102">SYNOPSIS</span></span>
<span data-ttu-id="a79b9-103">Invoca uma solicitação temporária de acesso à rede.</span><span class="sxs-lookup"><span data-stu-id="a79b9-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="a79b9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a79b9-104">SYNTAX</span></span>

### <span data-ttu-id="a79b9-105">ResourceGroupLevelResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a79b9-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a79b9-106">Resourceid</span><span class="sxs-lookup"><span data-stu-id="a79b9-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a79b9-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="a79b9-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a79b9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a79b9-108">DESCRIPTION</span></span>
<span data-ttu-id="a79b9-109">Invoca uma solicitação temporária de acesso à rede.</span><span class="sxs-lookup"><span data-stu-id="a79b9-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="a79b9-110">A solicitação é validada em relação à política de acesso de rede JIT configurada e, se permitido, abre uma conexão de rede de acordo com a solicitação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a79b9-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="a79b9-111">A solicitação será registrada na política para revisão posterior e será encerrada quando a duração especificada for excedida.</span><span class="sxs-lookup"><span data-stu-id="a79b9-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="a79b9-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a79b9-112">EXAMPLES</span></span>

### <span data-ttu-id="a79b9-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a79b9-113">Example 1</span></span>
```powershell
$MyResource = Get-AzResource -Id /subscriptions/xxxxxxx-xxxxx-xxxxx-xxxxxxx/resourceGroups/PolicyDemo/providers/Microsoft.Compute/virtualMachines/PolicyDemoVM1
$JitPolicy = (@{
        id    = $MyResource.ResourceId; 
        ports = (@{
                number                     = 22
                endTimeUtc                 = Get-Date (Get-Date -AsUTC).AddHours(1) -Format O
                allowedSourceAddressPrefix = @($MyPublicIP) 
            })
    })
$ActivationVM = @($JitPolicy)
Start-AzJitNetworkAccessPolicy -ResourceGroupName $($MyResource.ResourceGroupName) -Location $MyResource.Location -Name "default" -VirtualMachine $ActivationVM

```

<span data-ttu-id="a79b9-114">Abre uma conexão de rede por 1 hora pela porta 22 do meu IP público (não mostrado).</span><span class="sxs-lookup"><span data-stu-id="a79b9-114">Opens up a network connection for 1 hour over port 22 from my public IP (not shown).</span></span>

## <span data-ttu-id="a79b9-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a79b9-115">PARAMETERS</span></span>

### <span data-ttu-id="a79b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a79b9-116">-DefaultProfile</span></span>
<span data-ttu-id="a79b9-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a79b9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a79b9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a79b9-118">-InputObject</span></span>
<span data-ttu-id="a79b9-119">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="a79b9-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a79b9-120">-Local</span><span class="sxs-lookup"><span data-stu-id="a79b9-120">-Location</span></span>
<span data-ttu-id="a79b9-121">Localização.</span><span class="sxs-lookup"><span data-stu-id="a79b9-121">Location.</span></span>

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

### <span data-ttu-id="a79b9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a79b9-122">-Name</span></span>
<span data-ttu-id="a79b9-123">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a79b9-123">Resource name.</span></span>

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

### <span data-ttu-id="a79b9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a79b9-124">-ResourceGroupName</span></span>
<span data-ttu-id="a79b9-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a79b9-125">Resource group name.</span></span>

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

### <span data-ttu-id="a79b9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a79b9-126">-ResourceId</span></span>
<span data-ttu-id="a79b9-127">ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="a79b9-127">Resource ID.</span></span>

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

### <span data-ttu-id="a79b9-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a79b9-128">-VirtualMachine</span></span>
<span data-ttu-id="a79b9-129">Provisionamento Automático.</span><span class="sxs-lookup"><span data-stu-id="a79b9-129">Automatic Provisioning.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a79b9-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a79b9-130">-Confirm</span></span>
<span data-ttu-id="a79b9-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a79b9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a79b9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a79b9-132">-WhatIf</span></span>
<span data-ttu-id="a79b9-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a79b9-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a79b9-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a79b9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a79b9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a79b9-135">CommonParameters</span></span>
<span data-ttu-id="a79b9-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a79b9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a79b9-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a79b9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a79b9-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="a79b9-138">INPUTS</span></span>

### <span data-ttu-id="a79b9-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a79b9-139">System.String</span></span>

### <span data-ttu-id="a79b9-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="a79b9-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="a79b9-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="a79b9-141">OUTPUTS</span></span>

### <span data-ttu-id="a79b9-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a79b9-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="a79b9-143">Notas</span><span class="sxs-lookup"><span data-stu-id="a79b9-143">NOTES</span></span>

## <span data-ttu-id="a79b9-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a79b9-144">RELATED LINKS</span></span>
