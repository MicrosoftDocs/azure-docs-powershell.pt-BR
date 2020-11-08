---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: 5b2d10f3ffa2d00942b8198c598c9ec821dead99
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117585"
---
# <span data-ttu-id="467be-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="467be-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="467be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="467be-102">SYNOPSIS</span></span>
<span data-ttu-id="467be-103">Atualiza uma política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="467be-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="467be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="467be-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="467be-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="467be-105">DESCRIPTION</span></span>
<span data-ttu-id="467be-106">O cmdlet **set-AzServiceEndpointPolicy** cria uma política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="467be-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="467be-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="467be-107">EXAMPLES</span></span>

### <span data-ttu-id="467be-108">Exemplo 1: define uma política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="467be-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="467be-109">Esse comando atualiza uma política de ponto de extremidade de serviço chamada Policy1 definida pela $serviceEndpointPolicy do objeto pertencer ao o objeto de Resource "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="467be-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="467be-110">OS</span><span class="sxs-lookup"><span data-stu-id="467be-110">PARAMETERS</span></span>

### <span data-ttu-id="467be-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="467be-111">-DefaultProfile</span></span>
<span data-ttu-id="467be-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="467be-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="467be-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="467be-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="467be-114">O ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="467be-114">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="467be-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="467be-115">-Confirm</span></span>
<span data-ttu-id="467be-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="467be-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="467be-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="467be-117">-WhatIf</span></span>
<span data-ttu-id="467be-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="467be-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="467be-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="467be-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="467be-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="467be-120">CommonParameters</span></span>
<span data-ttu-id="467be-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="467be-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="467be-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="467be-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="467be-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="467be-123">INPUTS</span></span>

### <span data-ttu-id="467be-124">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="467be-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="467be-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="467be-125">OUTPUTS</span></span>

### <span data-ttu-id="467be-126">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="467be-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="467be-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="467be-127">NOTES</span></span>

## <span data-ttu-id="467be-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="467be-128">RELATED LINKS</span></span>

[<span data-ttu-id="467be-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="467be-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="467be-130">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="467be-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="467be-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="467be-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
