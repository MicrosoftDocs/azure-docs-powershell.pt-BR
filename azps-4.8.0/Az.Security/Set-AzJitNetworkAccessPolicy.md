---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: a316a59492034f0effd2d233ce386cbd6a256c75
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110887"
---
# <span data-ttu-id="242b6-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="242b6-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="242b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="242b6-102">SYNOPSIS</span></span>
<span data-ttu-id="242b6-103">Atualiza a política de acesso à rede JIT.</span><span class="sxs-lookup"><span data-stu-id="242b6-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="242b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="242b6-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="242b6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="242b6-105">DESCRIPTION</span></span>
<span data-ttu-id="242b6-106">Atualiza a política de acesso à rede JIT.</span><span class="sxs-lookup"><span data-stu-id="242b6-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="242b6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="242b6-107">EXAMPLES</span></span>

### <span data-ttu-id="242b6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="242b6-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="242b6-109">Atualiza uma política de acesso à rede JIT com novas regras de VM.</span><span class="sxs-lookup"><span data-stu-id="242b6-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="242b6-110">OS</span><span class="sxs-lookup"><span data-stu-id="242b6-110">PARAMETERS</span></span>

### <span data-ttu-id="242b6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="242b6-111">-DefaultProfile</span></span>
<span data-ttu-id="242b6-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="242b6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="242b6-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="242b6-113">-Kind</span></span>
<span data-ttu-id="242b6-114">Tipo.</span><span class="sxs-lookup"><span data-stu-id="242b6-114">Kind.</span></span>

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

### <span data-ttu-id="242b6-115">-Local</span><span class="sxs-lookup"><span data-stu-id="242b6-115">-Location</span></span>
<span data-ttu-id="242b6-116">Ponto.</span><span class="sxs-lookup"><span data-stu-id="242b6-116">Location.</span></span>

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

### <span data-ttu-id="242b6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="242b6-117">-Name</span></span>
<span data-ttu-id="242b6-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="242b6-118">Resource name.</span></span>

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

### <span data-ttu-id="242b6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="242b6-119">-ResourceGroupName</span></span>
<span data-ttu-id="242b6-120">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="242b6-120">Resource group name.</span></span>

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

### <span data-ttu-id="242b6-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="242b6-121">-VirtualMachine</span></span>
<span data-ttu-id="242b6-122">Máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="242b6-122">Virtual Machines.</span></span>

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

### <span data-ttu-id="242b6-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="242b6-123">-Confirm</span></span>
<span data-ttu-id="242b6-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="242b6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="242b6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="242b6-125">-WhatIf</span></span>
<span data-ttu-id="242b6-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="242b6-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="242b6-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="242b6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="242b6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="242b6-128">CommonParameters</span></span>
<span data-ttu-id="242b6-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="242b6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="242b6-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="242b6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="242b6-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="242b6-131">INPUTS</span></span>

### <span data-ttu-id="242b6-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="242b6-132">None</span></span>

## <span data-ttu-id="242b6-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="242b6-133">OUTPUTS</span></span>

### <span data-ttu-id="242b6-134">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="242b6-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="242b6-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="242b6-135">NOTES</span></span>

## <span data-ttu-id="242b6-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="242b6-136">RELATED LINKS</span></span>
