---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
ms.openlocfilehash: 56f0c3ec3a69819ad7faa28b10d33a3cf751c48f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429225"
---
# <span data-ttu-id="1f53f-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1f53f-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="1f53f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f53f-102">SYNOPSIS</span></span>
<span data-ttu-id="1f53f-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="1f53f-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f53f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f53f-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f53f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f53f-105">DESCRIPTION</span></span>
<span data-ttu-id="1f53f-106">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="1f53f-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="1f53f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f53f-107">EXAMPLES</span></span>

### <span data-ttu-id="1f53f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1f53f-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1f53f-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="1f53f-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="1f53f-110">OS</span><span class="sxs-lookup"><span data-stu-id="1f53f-110">PARAMETERS</span></span>

### <span data-ttu-id="1f53f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="1f53f-111">-Force</span></span>
<span data-ttu-id="1f53f-112">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="1f53f-112">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f53f-113">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1f53f-113">-RouteFilter</span></span>
<span data-ttu-id="1f53f-114">O RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1f53f-114">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f53f-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1f53f-115">-Confirm</span></span>
<span data-ttu-id="1f53f-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f53f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f53f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f53f-117">-WhatIf</span></span>
<span data-ttu-id="1f53f-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1f53f-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f53f-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f53f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f53f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f53f-120">-DefaultProfile</span></span>
<span data-ttu-id="1f53f-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f53f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f53f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f53f-122">CommonParameters</span></span>
<span data-ttu-id="1f53f-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f53f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f53f-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f53f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f53f-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f53f-125">INPUTS</span></span>

### <span data-ttu-id="1f53f-126">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1f53f-126">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1f53f-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f53f-127">OUTPUTS</span></span>

### <span data-ttu-id="1f53f-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1f53f-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1f53f-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f53f-129">NOTES</span></span>

## <span data-ttu-id="1f53f-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f53f-130">RELATED LINKS</span></span>

