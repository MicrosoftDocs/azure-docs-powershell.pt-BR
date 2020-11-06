---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
ms.openlocfilehash: f8b85088ac05cb118cf443eb54f28508727bd335
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441402"
---
# <span data-ttu-id="e21b3-101">Get-AzureRmCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="e21b3-101">Get-AzureRmCdnProfileResourceUsage</span></span>

## <span data-ttu-id="e21b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e21b3-102">SYNOPSIS</span></span>
<span data-ttu-id="e21b3-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="e21b3-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e21b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e21b3-104">SYNTAX</span></span>

### <span data-ttu-id="e21b3-105">Conjunto de parâmetros para parâmetros de campos (padrão)</span><span class="sxs-lookup"><span data-stu-id="e21b3-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e21b3-106">Conjunto de parâmetros para parâmetros de objeto</span><span class="sxs-lookup"><span data-stu-id="e21b3-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e21b3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e21b3-107">DESCRIPTION</span></span>
<span data-ttu-id="e21b3-108">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="e21b3-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="e21b3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e21b3-109">EXAMPLES</span></span>

### <span data-ttu-id="e21b3-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e21b3-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="e21b3-111">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="e21b3-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="e21b3-112">OS</span><span class="sxs-lookup"><span data-stu-id="e21b3-112">PARAMETERS</span></span>

### <span data-ttu-id="e21b3-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="e21b3-113">-CdnProfile</span></span>
<span data-ttu-id="e21b3-114">O objeto de perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="e21b3-114">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e21b3-115">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e21b3-115">-ProfileName</span></span>
<span data-ttu-id="e21b3-116">O nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="e21b3-116">The name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e21b3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e21b3-117">-ResourceGroupName</span></span>
<span data-ttu-id="e21b3-118">O grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="e21b3-118">The resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e21b3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e21b3-119">-DefaultProfile</span></span>
<span data-ttu-id="e21b3-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e21b3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e21b3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e21b3-121">CommonParameters</span></span>
<span data-ttu-id="e21b3-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e21b3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e21b3-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e21b3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e21b3-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e21b3-124">INPUTS</span></span>

### <span data-ttu-id="e21b3-125">Microsoft. Azure. Commands. cdn. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="e21b3-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="e21b3-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e21b3-126">OUTPUTS</span></span>

### <span data-ttu-id="e21b3-127">Microsoft. Azure. Commands. cdn. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="e21b3-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="e21b3-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e21b3-128">NOTES</span></span>

## <span data-ttu-id="e21b3-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e21b3-129">RELATED LINKS</span></span>

