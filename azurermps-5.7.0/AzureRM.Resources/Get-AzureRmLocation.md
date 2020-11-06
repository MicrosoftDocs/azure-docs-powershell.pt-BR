---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
ms.openlocfilehash: a3169a78747a34a831ed6bd738e5647c3a4d9eb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432415"
---
# <span data-ttu-id="6efea-101">Get-AzureRmLocation</span><span class="sxs-lookup"><span data-stu-id="6efea-101">Get-AzureRmLocation</span></span>

## <span data-ttu-id="6efea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6efea-102">SYNOPSIS</span></span>
<span data-ttu-id="6efea-103">Obtém todos os locais e os provedores de recursos com suporte para cada local.</span><span class="sxs-lookup"><span data-stu-id="6efea-103">Gets all locations and the supported resource providers for each location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6efea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6efea-104">SYNTAX</span></span>

```
Get-AzureRmLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6efea-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6efea-105">DESCRIPTION</span></span>
<span data-ttu-id="6efea-106">O cmdlet **Get-AzureRmLocation** Obtém todos os locais e os provedores de recursos com suporte para cada local.</span><span class="sxs-lookup"><span data-stu-id="6efea-106">The **Get-AzureRmLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="6efea-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6efea-107">EXAMPLES</span></span>

### <span data-ttu-id="6efea-108">Exemplo 1: obter todos os locais e os provedores de recursos com suporte</span><span class="sxs-lookup"><span data-stu-id="6efea-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzureRmLocation
```

<span data-ttu-id="6efea-109">Esse comando obtém todos os locais e os provedores de recursos com suporte para cada local.</span><span class="sxs-lookup"><span data-stu-id="6efea-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="6efea-110">OS</span><span class="sxs-lookup"><span data-stu-id="6efea-110">PARAMETERS</span></span>

### <span data-ttu-id="6efea-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6efea-111">-ApiVersion</span></span>
<span data-ttu-id="6efea-112">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="6efea-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="6efea-113">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="6efea-113">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6efea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6efea-114">-DefaultProfile</span></span>
<span data-ttu-id="6efea-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6efea-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6efea-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="6efea-116">-Pre</span></span>
<span data-ttu-id="6efea-117">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="6efea-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6efea-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6efea-118">CommonParameters</span></span>
<span data-ttu-id="6efea-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6efea-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6efea-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6efea-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6efea-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6efea-121">INPUTS</span></span>

### <span data-ttu-id="6efea-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6efea-122">None</span></span>
<span data-ttu-id="6efea-123">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="6efea-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6efea-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6efea-124">OUTPUTS</span></span>

### <span data-ttu-id="6efea-125">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceProviderLocation]</span><span class="sxs-lookup"><span data-stu-id="6efea-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation]</span></span>

## <span data-ttu-id="6efea-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6efea-126">NOTES</span></span>

## <span data-ttu-id="6efea-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6efea-127">RELATED LINKS</span></span>
