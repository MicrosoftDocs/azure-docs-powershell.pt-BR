---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
ms.openlocfilehash: a7c30ee436f35bee72e786c1d219e114236248da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432574"
---
# <span data-ttu-id="1d6f3-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="1d6f3-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="1d6f3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1d6f3-102">SYNOPSIS</span></span>
<span data-ttu-id="1d6f3-103">Obtém um provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="1d6f3-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d6f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d6f3-104">SYNTAX</span></span>

### <span data-ttu-id="1d6f3-105">ListAvailable (padrão)</span><span class="sxs-lookup"><span data-stu-id="1d6f3-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d6f3-106">Indivíduo</span><span class="sxs-lookup"><span data-stu-id="1d6f3-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d6f3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1d6f3-107">DESCRIPTION</span></span>
<span data-ttu-id="1d6f3-108">O cmdlet **Get-AzureRmResourceProvider** Obtém um provedor de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="1d6f3-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="1d6f3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d6f3-109">EXAMPLES</span></span>

## <span data-ttu-id="1d6f3-110">OS</span><span class="sxs-lookup"><span data-stu-id="1d6f3-110">PARAMETERS</span></span>

### <span data-ttu-id="1d6f3-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1d6f3-111">-ApiVersion</span></span>
<span data-ttu-id="1d6f3-112">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="1d6f3-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="1d6f3-113">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="1d6f3-113">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d6f3-114">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="1d6f3-114">-ListAvailable</span></span>
<span data-ttu-id="1d6f3-115">Indica que essa operação obtém todos os provedores de recursos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1d6f3-115">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d6f3-116">-Local</span><span class="sxs-lookup"><span data-stu-id="1d6f3-116">-Location</span></span>
<span data-ttu-id="1d6f3-117">Especifica o local do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="1d6f3-117">Specifies the location of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d6f3-118">-Pre</span><span class="sxs-lookup"><span data-stu-id="1d6f3-118">-Pre</span></span>
<span data-ttu-id="1d6f3-119">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="1d6f3-119">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1d6f3-120">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="1d6f3-120">-ProviderNamespace</span></span>
<span data-ttu-id="1d6f3-121">Especifica o namespace do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="1d6f3-121">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: IndividualProvider
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d6f3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d6f3-122">-DefaultProfile</span></span>
<span data-ttu-id="1d6f3-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1d6f3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d6f3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d6f3-124">CommonParameters</span></span>
<span data-ttu-id="1d6f3-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d6f3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d6f3-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d6f3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d6f3-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1d6f3-127">INPUTS</span></span>

## <span data-ttu-id="1d6f3-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1d6f3-128">OUTPUTS</span></span>

### <span data-ttu-id="1d6f3-129">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="1d6f3-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="1d6f3-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1d6f3-130">NOTES</span></span>

## <span data-ttu-id="1d6f3-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d6f3-131">RELATED LINKS</span></span>

[<span data-ttu-id="1d6f3-132">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="1d6f3-132">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="1d6f3-133">Cancelar registro-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="1d6f3-133">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


