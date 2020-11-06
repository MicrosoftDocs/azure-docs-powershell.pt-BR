---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 62dccdc3b55caa5d63036ed3298caa5a01514342
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432734"
---
# <span data-ttu-id="3b331-101">Start-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3b331-101">Start-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="3b331-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b331-102">SYNOPSIS</span></span>
<span data-ttu-id="3b331-103">Invoca uma solicitação de acesso temporário à rede.</span><span class="sxs-lookup"><span data-stu-id="3b331-103">Invokes a temporary network access request.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b331-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b331-104">SYNTAX</span></span>

### <span data-ttu-id="3b331-105">ResourceGroupLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="3b331-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b331-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="3b331-106">ResourceId</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b331-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="3b331-107">InputObject</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b331-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3b331-108">DESCRIPTION</span></span>
<span data-ttu-id="3b331-109">Invoca uma solicitação de acesso temporário à rede.</span><span class="sxs-lookup"><span data-stu-id="3b331-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="3b331-110">A solicitação é validada em relação à política de acesso à rede JIT configurada e, se permittet, abre uma conexão de rede de acordo com a solicitação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3b331-110">The request is validated against the configured JIT network access policy and if permittet, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="3b331-111">A solicitação será logedda na política para revisão posterior e será encerrada quando a duração especificada for excedida.</span><span class="sxs-lookup"><span data-stu-id="3b331-111">The request will be loged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="3b331-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3b331-112">EXAMPLES</span></span>

### <span data-ttu-id="3b331-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3b331-113">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -Kind "Basic" -VirtualMachine $vms

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.S
                    ecurity/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                    Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="3b331-114">Abre uma conexão de rede de acordo com os dados de solicitação de conexão especificados.</span><span class="sxs-lookup"><span data-stu-id="3b331-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="3b331-115">OS</span><span class="sxs-lookup"><span data-stu-id="3b331-115">PARAMETERS</span></span>

### <span data-ttu-id="3b331-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b331-116">-DefaultProfile</span></span>
<span data-ttu-id="3b331-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3b331-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b331-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b331-118">-InputObject</span></span>
<span data-ttu-id="3b331-119">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="3b331-119">Input Object.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyInitiateInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b331-120">-Local</span><span class="sxs-lookup"><span data-stu-id="3b331-120">-Location</span></span>
<span data-ttu-id="3b331-121">Ponto.</span><span class="sxs-lookup"><span data-stu-id="3b331-121">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b331-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3b331-122">-Name</span></span>
<span data-ttu-id="3b331-123">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="3b331-123">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b331-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b331-124">-ResourceGroupName</span></span>
<span data-ttu-id="3b331-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3b331-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b331-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b331-126">-ResourceId</span></span>
<span data-ttu-id="3b331-127">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="3b331-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b331-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3b331-128">-VirtualMachine</span></span>
<span data-ttu-id="3b331-129">Provisionamento automático.</span><span class="sxs-lookup"><span data-stu-id="3b331-129">Automatic Provisioning.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b331-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3b331-130">-Confirm</span></span>
<span data-ttu-id="3b331-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b331-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b331-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b331-132">-WhatIf</span></span>
<span data-ttu-id="3b331-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3b331-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b331-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3b331-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b331-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b331-135">CommonParameters</span></span>
<span data-ttu-id="3b331-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b331-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b331-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b331-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b331-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3b331-138">INPUTS</span></span>

### <span data-ttu-id="3b331-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3b331-139">System.String</span></span>
<span data-ttu-id="3b331-140">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine []</span><span class="sxs-lookup"><span data-stu-id="3b331-140">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]</span></span>

## <span data-ttu-id="3b331-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3b331-141">OUTPUTS</span></span>

### <span data-ttu-id="3b331-142">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3b331-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="3b331-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3b331-143">NOTES</span></span>

## <span data-ttu-id="3b331-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b331-144">RELATED LINKS</span></span>
