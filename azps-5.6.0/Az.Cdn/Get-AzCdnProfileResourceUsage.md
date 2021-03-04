---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 1a4e3f08653f6c7bda799b55618caff4e77fe7bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892225"
---
# <span data-ttu-id="1943e-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="1943e-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="1943e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1943e-102">SYNOPSIS</span></span>
<span data-ttu-id="1943e-103">Obtém o uso de recursos de um perfil cdn.</span><span class="sxs-lookup"><span data-stu-id="1943e-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="1943e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1943e-104">SYNTAX</span></span>

### <span data-ttu-id="1943e-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1943e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1943e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1943e-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1943e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1943e-107">DESCRIPTION</span></span>
<span data-ttu-id="1943e-108">{{Preencha a Descrição}}</span><span class="sxs-lookup"><span data-stu-id="1943e-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="1943e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1943e-109">EXAMPLES</span></span>

### <span data-ttu-id="1943e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1943e-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1943e-111">{{ Adicione a descrição do exemplo aqui }}</span><span class="sxs-lookup"><span data-stu-id="1943e-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="1943e-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1943e-112">PARAMETERS</span></span>

### <span data-ttu-id="1943e-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="1943e-113">-CdnProfile</span></span>
<span data-ttu-id="1943e-114">O objeto de perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="1943e-114">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1943e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1943e-115">-DefaultProfile</span></span>
<span data-ttu-id="1943e-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1943e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1943e-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="1943e-117">-ProfileName</span></span>
<span data-ttu-id="1943e-118">O nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="1943e-118">The name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1943e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1943e-119">-ResourceGroupName</span></span>
<span data-ttu-id="1943e-120">O grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="1943e-120">The resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1943e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1943e-121">CommonParameters</span></span>
<span data-ttu-id="1943e-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1943e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1943e-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1943e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1943e-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1943e-124">INPUTS</span></span>

### <span data-ttu-id="1943e-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="1943e-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="1943e-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1943e-126">OUTPUTS</span></span>

### <span data-ttu-id="1943e-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="1943e-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="1943e-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="1943e-128">NOTES</span></span>

## <span data-ttu-id="1943e-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1943e-129">RELATED LINKS</span></span>
