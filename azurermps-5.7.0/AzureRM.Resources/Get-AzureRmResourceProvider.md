---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
ms.openlocfilehash: 54ce1d9fa73b29318597f5a1442712aabf7f92b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426621"
---
# <span data-ttu-id="5f621-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5f621-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="5f621-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f621-102">SYNOPSIS</span></span>
<span data-ttu-id="5f621-103">Obtém um provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="5f621-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f621-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f621-104">SYNTAX</span></span>

### <span data-ttu-id="5f621-105">ListAvailable (padrão)</span><span class="sxs-lookup"><span data-stu-id="5f621-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f621-106">Indivíduo</span><span class="sxs-lookup"><span data-stu-id="5f621-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f621-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5f621-107">DESCRIPTION</span></span>
<span data-ttu-id="5f621-108">O cmdlet **Get-AzureRmResourceProvider** Obtém um provedor de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="5f621-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="5f621-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5f621-109">EXAMPLES</span></span>

## <span data-ttu-id="5f621-110">OS</span><span class="sxs-lookup"><span data-stu-id="5f621-110">PARAMETERS</span></span>

### <span data-ttu-id="5f621-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5f621-111">-ApiVersion</span></span>
<span data-ttu-id="5f621-112">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="5f621-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="5f621-113">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="5f621-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="5f621-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f621-114">-DefaultProfile</span></span>
<span data-ttu-id="5f621-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5f621-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f621-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="5f621-116">-ListAvailable</span></span>
<span data-ttu-id="5f621-117">Indica que essa operação obtém todos os provedores de recursos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="5f621-117">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f621-118">-Local</span><span class="sxs-lookup"><span data-stu-id="5f621-118">-Location</span></span>
<span data-ttu-id="5f621-119">Especifica o local do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="5f621-119">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="5f621-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="5f621-120">-Pre</span></span>
<span data-ttu-id="5f621-121">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="5f621-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5f621-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="5f621-122">-ProviderNamespace</span></span>
<span data-ttu-id="5f621-123">Especifica o namespace do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="5f621-123">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: String
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f621-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f621-124">CommonParameters</span></span>
<span data-ttu-id="5f621-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f621-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f621-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f621-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f621-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5f621-127">INPUTS</span></span>

### <span data-ttu-id="5f621-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5f621-128">None</span></span>
<span data-ttu-id="5f621-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="5f621-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5f621-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5f621-130">OUTPUTS</span></span>

### <span data-ttu-id="5f621-131">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5f621-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="5f621-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5f621-132">NOTES</span></span>

## <span data-ttu-id="5f621-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f621-133">RELATED LINKS</span></span>

[<span data-ttu-id="5f621-134">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5f621-134">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="5f621-135">Cancelar registro-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5f621-135">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


