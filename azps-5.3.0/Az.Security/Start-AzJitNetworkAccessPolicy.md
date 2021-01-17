---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 0efde69aec3b30c58aee8c42aeb1703215219c2e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433230"
---
# <span data-ttu-id="06f95-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="06f95-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="06f95-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06f95-102">SYNOPSIS</span></span>
<span data-ttu-id="06f95-103">Invoca uma solicitação de acesso temporário à rede.</span><span class="sxs-lookup"><span data-stu-id="06f95-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="06f95-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06f95-104">SYNTAX</span></span>

### <span data-ttu-id="06f95-105">ResourceGroupLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="06f95-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06f95-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="06f95-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06f95-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="06f95-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06f95-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06f95-108">DESCRIPTION</span></span>
<span data-ttu-id="06f95-109">Invoca uma solicitação de acesso temporário à rede.</span><span class="sxs-lookup"><span data-stu-id="06f95-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="06f95-110">A solicitação é validada em relação à política de acesso à rede JIT configurada e, se permitido, abre uma conexão de rede de acordo com a solicitação do usuário.</span><span class="sxs-lookup"><span data-stu-id="06f95-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="06f95-111">A solicitação será registrada na política para revisão posterior e será terminada quando a duração especificada for excedida.</span><span class="sxs-lookup"><span data-stu-id="06f95-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="06f95-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06f95-112">EXAMPLES</span></span>

### <span data-ttu-id="06f95-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="06f95-113">Example 1</span></span>
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

<span data-ttu-id="06f95-114">Abre uma conexão de rede por uma hora na porta 22 do meu IP público (não mostrado).</span><span class="sxs-lookup"><span data-stu-id="06f95-114">Opens up a network connection for 1 hour over port 22 from my public IP (not shown).</span></span>

## <span data-ttu-id="06f95-115">OS</span><span class="sxs-lookup"><span data-stu-id="06f95-115">PARAMETERS</span></span>

### <span data-ttu-id="06f95-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06f95-116">-DefaultProfile</span></span>
<span data-ttu-id="06f95-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06f95-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06f95-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06f95-118">-InputObject</span></span>
<span data-ttu-id="06f95-119">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="06f95-119">Input Object.</span></span>

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

### <span data-ttu-id="06f95-120">-Local</span><span class="sxs-lookup"><span data-stu-id="06f95-120">-Location</span></span>
<span data-ttu-id="06f95-121">Ponto.</span><span class="sxs-lookup"><span data-stu-id="06f95-121">Location.</span></span>

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

### <span data-ttu-id="06f95-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="06f95-122">-Name</span></span>
<span data-ttu-id="06f95-123">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="06f95-123">Resource name.</span></span>

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

### <span data-ttu-id="06f95-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06f95-124">-ResourceGroupName</span></span>
<span data-ttu-id="06f95-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="06f95-125">Resource group name.</span></span>

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

### <span data-ttu-id="06f95-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06f95-126">-ResourceId</span></span>
<span data-ttu-id="06f95-127">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="06f95-127">Resource ID.</span></span>

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

### <span data-ttu-id="06f95-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="06f95-128">-VirtualMachine</span></span>
<span data-ttu-id="06f95-129">Provisionamento automático.</span><span class="sxs-lookup"><span data-stu-id="06f95-129">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="06f95-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="06f95-130">-Confirm</span></span>
<span data-ttu-id="06f95-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06f95-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06f95-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06f95-132">-WhatIf</span></span>
<span data-ttu-id="06f95-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="06f95-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06f95-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="06f95-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06f95-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06f95-135">CommonParameters</span></span>
<span data-ttu-id="06f95-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06f95-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06f95-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06f95-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06f95-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06f95-138">INPUTS</span></span>

### <span data-ttu-id="06f95-139">System. String</span><span class="sxs-lookup"><span data-stu-id="06f95-139">System.String</span></span>

### <span data-ttu-id="06f95-140">Microsoft. Azure. Commands. Security. cmdlets. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="06f95-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="06f95-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06f95-141">OUTPUTS</span></span>

### <span data-ttu-id="06f95-142">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="06f95-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="06f95-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06f95-143">NOTES</span></span>

## <span data-ttu-id="06f95-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06f95-144">RELATED LINKS</span></span>
