---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 72e3cf48f112c5e9bb07a8f7eb57dfe3d4c9ee07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429341"
---
# <span data-ttu-id="1f89c-101">Set-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1f89c-101">Set-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="1f89c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f89c-102">SYNOPSIS</span></span>
<span data-ttu-id="1f89c-103">Atualiza a política de acesso à rede JIT.</span><span class="sxs-lookup"><span data-stu-id="1f89c-103">Updates JIT network access policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f89c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f89c-104">SYNTAX</span></span>

```
Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f89c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f89c-105">DESCRIPTION</span></span>
<span data-ttu-id="1f89c-106">Atualiza a política de acesso à rede JIT.</span><span class="sxs-lookup"><span data-stu-id="1f89c-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="1f89c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f89c-107">EXAMPLES</span></span>

### <span data-ttu-id="1f89c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1f89c-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="1f89c-109">Atualiza uma política de acesso à rede JIT com novas regras de VM.</span><span class="sxs-lookup"><span data-stu-id="1f89c-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="1f89c-110">OS</span><span class="sxs-lookup"><span data-stu-id="1f89c-110">PARAMETERS</span></span>

### <span data-ttu-id="1f89c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f89c-111">-DefaultProfile</span></span>
<span data-ttu-id="1f89c-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f89c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f89c-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="1f89c-113">-Kind</span></span>
<span data-ttu-id="1f89c-114">Tipo.</span><span class="sxs-lookup"><span data-stu-id="1f89c-114">Kind.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f89c-115">-Local</span><span class="sxs-lookup"><span data-stu-id="1f89c-115">-Location</span></span>
<span data-ttu-id="1f89c-116">Ponto.</span><span class="sxs-lookup"><span data-stu-id="1f89c-116">Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f89c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f89c-117">-Name</span></span>
<span data-ttu-id="1f89c-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="1f89c-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f89c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f89c-119">-ResourceGroupName</span></span>
<span data-ttu-id="1f89c-120">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1f89c-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f89c-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1f89c-121">-VirtualMachine</span></span>
<span data-ttu-id="1f89c-122">Máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="1f89c-122">Virutal Machines.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyVirtualMachine[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f89c-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1f89c-123">-Confirm</span></span>
<span data-ttu-id="1f89c-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f89c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f89c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f89c-125">-WhatIf</span></span>
<span data-ttu-id="1f89c-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1f89c-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f89c-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f89c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f89c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f89c-128">CommonParameters</span></span>
<span data-ttu-id="1f89c-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f89c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f89c-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f89c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f89c-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f89c-131">INPUTS</span></span>

### <span data-ttu-id="1f89c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1f89c-132">System.String</span></span>
<span data-ttu-id="1f89c-133">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyVirtualMachine []</span><span class="sxs-lookup"><span data-stu-id="1f89c-133">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyVirtualMachine[]</span></span>

## <span data-ttu-id="1f89c-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f89c-134">OUTPUTS</span></span>

### <span data-ttu-id="1f89c-135">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1f89c-135">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="1f89c-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f89c-136">NOTES</span></span>

## <span data-ttu-id="1f89c-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f89c-137">RELATED LINKS</span></span>
