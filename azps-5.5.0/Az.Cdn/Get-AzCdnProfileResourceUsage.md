---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 8395fc4d90eb4e6d38eda18753761a1bf2598479
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117911"
---
# <span data-ttu-id="2d73a-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="2d73a-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="2d73a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d73a-102">SYNOPSIS</span></span>
<span data-ttu-id="2d73a-103">Obtém o uso do recurso de um perfil de CDN.</span><span class="sxs-lookup"><span data-stu-id="2d73a-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="2d73a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d73a-104">SYNTAX</span></span>

### <span data-ttu-id="2d73a-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2d73a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d73a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d73a-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d73a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2d73a-107">DESCRIPTION</span></span>
<span data-ttu-id="2d73a-108">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="2d73a-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="2d73a-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2d73a-109">EXAMPLES</span></span>

### <span data-ttu-id="2d73a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2d73a-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="2d73a-111">{{ Adicione a descrição do exemplo aqui }}</span><span class="sxs-lookup"><span data-stu-id="2d73a-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="2d73a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d73a-112">PARAMETERS</span></span>

### <span data-ttu-id="2d73a-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="2d73a-113">-CdnProfile</span></span>
<span data-ttu-id="2d73a-114">O objeto de perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="2d73a-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="2d73a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d73a-115">-DefaultProfile</span></span>
<span data-ttu-id="2d73a-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="2d73a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d73a-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2d73a-117">-ProfileName</span></span>
<span data-ttu-id="2d73a-118">O nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="2d73a-118">The name of the profile.</span></span>

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

### <span data-ttu-id="2d73a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d73a-119">-ResourceGroupName</span></span>
<span data-ttu-id="2d73a-120">O grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="2d73a-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="2d73a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d73a-121">CommonParameters</span></span>
<span data-ttu-id="2d73a-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d73a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d73a-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d73a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d73a-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="2d73a-124">INPUTS</span></span>

### <span data-ttu-id="2d73a-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="2d73a-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="2d73a-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="2d73a-126">OUTPUTS</span></span>

### <span data-ttu-id="2d73a-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="2d73a-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="2d73a-128">Notas</span><span class="sxs-lookup"><span data-stu-id="2d73a-128">NOTES</span></span>

## <span data-ttu-id="2d73a-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d73a-129">RELATED LINKS</span></span>
