---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: 75cf6bac1913a2baa55a28135ba2d59f5ceaa07f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599967"
---
# <span data-ttu-id="fb203-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="fb203-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="fb203-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb203-102">SYNOPSIS</span></span>
<span data-ttu-id="fb203-103">Atualiza uma política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="fb203-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="fb203-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb203-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb203-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb203-105">DESCRIPTION</span></span>
<span data-ttu-id="fb203-106">O cmdlet **set-AzServiceEndpointPolicy** cria uma política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="fb203-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="fb203-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb203-107">EXAMPLES</span></span>

### <span data-ttu-id="fb203-108">Exemplo 1: define uma política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="fb203-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="fb203-109">Esse comando atualiza uma política de ponto de extremidade de serviço chamada Policy1 definida pela $serviceEndpointPolicy do objeto pertencer ao o objeto de Resource "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="fb203-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="fb203-110">OS</span><span class="sxs-lookup"><span data-stu-id="fb203-110">PARAMETERS</span></span>

### <span data-ttu-id="fb203-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb203-111">-DefaultProfile</span></span>
<span data-ttu-id="fb203-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb203-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb203-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="fb203-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="fb203-114">O ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="fb203-114">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="fb203-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fb203-115">-Confirm</span></span>
<span data-ttu-id="fb203-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb203-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb203-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb203-117">-WhatIf</span></span>
<span data-ttu-id="fb203-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fb203-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb203-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb203-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb203-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb203-120">CommonParameters</span></span>
<span data-ttu-id="fb203-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb203-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb203-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb203-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb203-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb203-123">INPUTS</span></span>

### <span data-ttu-id="fb203-124">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="fb203-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="fb203-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb203-125">OUTPUTS</span></span>

### <span data-ttu-id="fb203-126">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="fb203-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="fb203-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb203-127">NOTES</span></span>

## <span data-ttu-id="fb203-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb203-128">RELATED LINKS</span></span>

[<span data-ttu-id="fb203-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="fb203-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="fb203-130">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="fb203-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="fb203-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="fb203-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
