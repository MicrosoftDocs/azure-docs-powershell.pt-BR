---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: e8cf8b2abebd20b514d0bae2ad220d3e702f04f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892740"
---
# <span data-ttu-id="a3d36-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a3d36-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="a3d36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3d36-102">SYNOPSIS</span></span>
<span data-ttu-id="a3d36-103">Atualiza uma política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="a3d36-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="a3d36-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a3d36-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3d36-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a3d36-105">DESCRIPTION</span></span>
<span data-ttu-id="a3d36-106">O cmdlet **Set-AzServiceEndpointPolicy** cria uma política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="a3d36-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="a3d36-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3d36-107">EXAMPLES</span></span>

### <span data-ttu-id="a3d36-108">Exemplo 1: define uma política de ponto de extremidade de serviço</span><span class="sxs-lookup"><span data-stu-id="a3d36-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="a3d36-109">Este comando atualiza uma política de ponto de extremidade de serviço chamada Policy1 definida pelo objeto $serviceEndpointPolicy pertencem ao grupo de recursos "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="a3d36-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="a3d36-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a3d36-110">PARAMETERS</span></span>

### <span data-ttu-id="a3d36-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3d36-111">-DefaultProfile</span></span>
<span data-ttu-id="a3d36-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a3d36-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3d36-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a3d36-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="a3d36-114">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a3d36-114">The ServiceEndpointPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3d36-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3d36-115">-Confirm</span></span>
<span data-ttu-id="a3d36-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3d36-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3d36-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3d36-117">-WhatIf</span></span>
<span data-ttu-id="a3d36-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a3d36-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3d36-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a3d36-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3d36-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3d36-120">CommonParameters</span></span>
<span data-ttu-id="a3d36-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3d36-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3d36-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3d36-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3d36-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3d36-123">INPUTS</span></span>

### <span data-ttu-id="a3d36-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a3d36-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="a3d36-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a3d36-125">OUTPUTS</span></span>

### <span data-ttu-id="a3d36-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a3d36-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="a3d36-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="a3d36-127">NOTES</span></span>

## <span data-ttu-id="a3d36-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3d36-128">RELATED LINKS</span></span>

[<span data-ttu-id="a3d36-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a3d36-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="a3d36-130">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a3d36-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="a3d36-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a3d36-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
