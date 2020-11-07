---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 8395fc4d90eb4e6d38eda18753761a1bf2598479
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943455"
---
# <span data-ttu-id="7f0fe-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="7f0fe-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="7f0fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f0fe-102">SYNOPSIS</span></span>
<span data-ttu-id="7f0fe-103">Obtém o uso do recurso de um perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="7f0fe-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="7f0fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f0fe-104">SYNTAX</span></span>

### <span data-ttu-id="7f0fe-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7f0fe-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f0fe-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f0fe-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f0fe-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f0fe-107">DESCRIPTION</span></span>
<span data-ttu-id="7f0fe-108">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="7f0fe-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="7f0fe-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f0fe-109">EXAMPLES</span></span>

### <span data-ttu-id="7f0fe-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7f0fe-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="7f0fe-111">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="7f0fe-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="7f0fe-112">OS</span><span class="sxs-lookup"><span data-stu-id="7f0fe-112">PARAMETERS</span></span>

### <span data-ttu-id="7f0fe-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="7f0fe-113">-CdnProfile</span></span>
<span data-ttu-id="7f0fe-114">O objeto de perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="7f0fe-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="7f0fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f0fe-115">-DefaultProfile</span></span>
<span data-ttu-id="7f0fe-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7f0fe-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f0fe-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="7f0fe-117">-ProfileName</span></span>
<span data-ttu-id="7f0fe-118">O nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="7f0fe-118">The name of the profile.</span></span>

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

### <span data-ttu-id="7f0fe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f0fe-119">-ResourceGroupName</span></span>
<span data-ttu-id="7f0fe-120">O grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="7f0fe-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="7f0fe-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f0fe-121">CommonParameters</span></span>
<span data-ttu-id="7f0fe-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f0fe-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f0fe-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f0fe-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f0fe-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f0fe-124">INPUTS</span></span>

### <span data-ttu-id="7f0fe-125">Microsoft. Azure. Commands. cdn. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="7f0fe-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="7f0fe-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f0fe-126">OUTPUTS</span></span>

### <span data-ttu-id="7f0fe-127">Microsoft. Azure. Commands. cdn. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="7f0fe-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="7f0fe-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f0fe-128">NOTES</span></span>

## <span data-ttu-id="7f0fe-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f0fe-129">RELATED LINKS</span></span>
