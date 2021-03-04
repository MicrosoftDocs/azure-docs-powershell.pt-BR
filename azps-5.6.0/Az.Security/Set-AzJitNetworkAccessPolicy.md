---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 0588929d8f45c04275e2d79823ed86c9db787060
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888607"
---
# <span data-ttu-id="9fdf5-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9fdf5-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="9fdf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fdf5-102">SYNOPSIS</span></span>
<span data-ttu-id="9fdf5-103">Atualiza a política de acesso à rede JIT.</span><span class="sxs-lookup"><span data-stu-id="9fdf5-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="9fdf5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9fdf5-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fdf5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9fdf5-105">DESCRIPTION</span></span>
<span data-ttu-id="9fdf5-106">Atualiza a política de acesso à rede JIT.</span><span class="sxs-lookup"><span data-stu-id="9fdf5-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="9fdf5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9fdf5-107">EXAMPLES</span></span>

### <span data-ttu-id="9fdf5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9fdf5-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="9fdf5-109">Atualiza uma política de acesso à rede JIT com novas regras de VM.</span><span class="sxs-lookup"><span data-stu-id="9fdf5-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="9fdf5-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9fdf5-110">PARAMETERS</span></span>

### <span data-ttu-id="9fdf5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fdf5-111">-DefaultProfile</span></span>
<span data-ttu-id="9fdf5-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9fdf5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fdf5-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="9fdf5-113">-Kind</span></span>
<span data-ttu-id="9fdf5-114">Jit Network Access Policy Kind.</span><span class="sxs-lookup"><span data-stu-id="9fdf5-114">Jit Network Access Policy Kind.</span></span>

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

### <span data-ttu-id="9fdf5-115">-Location</span><span class="sxs-lookup"><span data-stu-id="9fdf5-115">-Location</span></span>
<span data-ttu-id="9fdf5-116">Local.</span><span class="sxs-lookup"><span data-stu-id="9fdf5-116">Location.</span></span>

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

### <span data-ttu-id="9fdf5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9fdf5-117">-Name</span></span>
<span data-ttu-id="9fdf5-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="9fdf5-118">Resource name.</span></span>

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

### <span data-ttu-id="9fdf5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fdf5-119">-ResourceGroupName</span></span>
<span data-ttu-id="9fdf5-120">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9fdf5-120">Resource group name.</span></span>

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

### <span data-ttu-id="9fdf5-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9fdf5-121">-VirtualMachine</span></span>
<span data-ttu-id="9fdf5-122">Máquinas Virtuais.</span><span class="sxs-lookup"><span data-stu-id="9fdf5-122">Virtual Machines.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyVirtualMachine[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fdf5-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9fdf5-123">-Confirm</span></span>
<span data-ttu-id="9fdf5-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fdf5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fdf5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fdf5-125">-WhatIf</span></span>
<span data-ttu-id="9fdf5-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9fdf5-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9fdf5-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9fdf5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fdf5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fdf5-128">CommonParameters</span></span>
<span data-ttu-id="9fdf5-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fdf5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fdf5-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9fdf5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fdf5-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9fdf5-131">INPUTS</span></span>

### <span data-ttu-id="9fdf5-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9fdf5-132">None</span></span>

## <span data-ttu-id="9fdf5-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9fdf5-133">OUTPUTS</span></span>

### <span data-ttu-id="9fdf5-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9fdf5-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="9fdf5-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="9fdf5-135">NOTES</span></span>

## <span data-ttu-id="9fdf5-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9fdf5-136">RELATED LINKS</span></span>
