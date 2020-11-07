---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 188d653f58644a359f20886e96791efa53ab7b2a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772491"
---
# <span data-ttu-id="dd27a-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dd27a-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="dd27a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd27a-102">SYNOPSIS</span></span>
<span data-ttu-id="dd27a-103">Invoca uma solicitação de acesso temporário à rede.</span><span class="sxs-lookup"><span data-stu-id="dd27a-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="dd27a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd27a-104">SYNTAX</span></span>

### <span data-ttu-id="dd27a-105">ResourceGroupLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="dd27a-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd27a-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="dd27a-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd27a-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="dd27a-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd27a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd27a-108">DESCRIPTION</span></span>
<span data-ttu-id="dd27a-109">Invoca uma solicitação de acesso temporário à rede.</span><span class="sxs-lookup"><span data-stu-id="dd27a-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="dd27a-110">A solicitação é validada em relação à política de acesso à rede JIT configurada e, se permitido, abre uma conexão de rede de acordo com a solicitação do usuário.</span><span class="sxs-lookup"><span data-stu-id="dd27a-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="dd27a-111">A solicitação será registrada na política para revisão posterior e será terminada quando a duração especificada for excedida.</span><span class="sxs-lookup"><span data-stu-id="dd27a-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="dd27a-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd27a-112">EXAMPLES</span></span>

### <span data-ttu-id="dd27a-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dd27a-113">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -Kind "Basic" -VirtualMachine $vms

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.S
                    ecurity/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                    Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="dd27a-114">Abre uma conexão de rede de acordo com os dados de solicitação de conexão especificados.</span><span class="sxs-lookup"><span data-stu-id="dd27a-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="dd27a-115">OS</span><span class="sxs-lookup"><span data-stu-id="dd27a-115">PARAMETERS</span></span>

### <span data-ttu-id="dd27a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd27a-116">-DefaultProfile</span></span>
<span data-ttu-id="dd27a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dd27a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd27a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd27a-118">-InputObject</span></span>
<span data-ttu-id="dd27a-119">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="dd27a-119">Input Object.</span></span>

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

### <span data-ttu-id="dd27a-120">-Local</span><span class="sxs-lookup"><span data-stu-id="dd27a-120">-Location</span></span>
<span data-ttu-id="dd27a-121">Ponto.</span><span class="sxs-lookup"><span data-stu-id="dd27a-121">Location.</span></span>

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

### <span data-ttu-id="dd27a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd27a-122">-Name</span></span>
<span data-ttu-id="dd27a-123">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="dd27a-123">Resource name.</span></span>

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

### <span data-ttu-id="dd27a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd27a-124">-ResourceGroupName</span></span>
<span data-ttu-id="dd27a-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dd27a-125">Resource group name.</span></span>

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

### <span data-ttu-id="dd27a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd27a-126">-ResourceId</span></span>
<span data-ttu-id="dd27a-127">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="dd27a-127">Resource ID.</span></span>

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

### <span data-ttu-id="dd27a-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dd27a-128">-VirtualMachine</span></span>
<span data-ttu-id="dd27a-129">Provisionamento automático.</span><span class="sxs-lookup"><span data-stu-id="dd27a-129">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="dd27a-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dd27a-130">-Confirm</span></span>
<span data-ttu-id="dd27a-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd27a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd27a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd27a-132">-WhatIf</span></span>
<span data-ttu-id="dd27a-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dd27a-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd27a-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dd27a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd27a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd27a-135">CommonParameters</span></span>
<span data-ttu-id="dd27a-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd27a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd27a-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd27a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd27a-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd27a-138">INPUTS</span></span>

### <span data-ttu-id="dd27a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dd27a-139">System.String</span></span>

### <span data-ttu-id="dd27a-140">Microsoft. Azure. Commands. Security. cmdlets. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="dd27a-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="dd27a-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd27a-141">OUTPUTS</span></span>

### <span data-ttu-id="dd27a-142">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dd27a-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="dd27a-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd27a-143">NOTES</span></span>

## <span data-ttu-id="dd27a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd27a-144">RELATED LINKS</span></span>