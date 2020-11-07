---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourceprovider
schema: 2.0.0
ms.openlocfilehash: ca4f9431a7b382166b99a33be5b9373871b610e8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785294"
---
# <span data-ttu-id="38a0b-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="38a0b-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="38a0b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38a0b-102">SYNOPSIS</span></span>
<span data-ttu-id="38a0b-103">Obtém um provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="38a0b-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38a0b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38a0b-104">SYNTAX</span></span>

### <span data-ttu-id="38a0b-105">ListAvailable (padrão)</span><span class="sxs-lookup"><span data-stu-id="38a0b-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38a0b-106">Indivíduo</span><span class="sxs-lookup"><span data-stu-id="38a0b-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38a0b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="38a0b-107">DESCRIPTION</span></span>
<span data-ttu-id="38a0b-108">O cmdlet **Get-AzureRmResourceProvider** Obtém um provedor de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="38a0b-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="38a0b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38a0b-109">EXAMPLES</span></span>

## <span data-ttu-id="38a0b-110">OS</span><span class="sxs-lookup"><span data-stu-id="38a0b-110">PARAMETERS</span></span>

### <span data-ttu-id="38a0b-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="38a0b-111">-ApiVersion</span></span>
<span data-ttu-id="38a0b-112">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="38a0b-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="38a0b-113">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="38a0b-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="38a0b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38a0b-114">-DefaultProfile</span></span>
<span data-ttu-id="38a0b-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="38a0b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38a0b-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="38a0b-116">-ListAvailable</span></span>
<span data-ttu-id="38a0b-117">Indica que essa operação obtém todos os provedores de recursos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="38a0b-117">Indicates that this operation gets all available resource providers.</span></span>

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

### <span data-ttu-id="38a0b-118">-Local</span><span class="sxs-lookup"><span data-stu-id="38a0b-118">-Location</span></span>
<span data-ttu-id="38a0b-119">Especifica o local do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="38a0b-119">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="38a0b-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="38a0b-120">-Pre</span></span>
<span data-ttu-id="38a0b-121">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="38a0b-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="38a0b-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="38a0b-122">-ProviderNamespace</span></span>
<span data-ttu-id="38a0b-123">Especifica o namespace do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="38a0b-123">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38a0b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a0b-124">CommonParameters</span></span>
<span data-ttu-id="38a0b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38a0b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38a0b-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38a0b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a0b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="38a0b-127">INPUTS</span></span>

## <span data-ttu-id="38a0b-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="38a0b-128">OUTPUTS</span></span>

## <span data-ttu-id="38a0b-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="38a0b-129">NOTES</span></span>

## <span data-ttu-id="38a0b-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38a0b-130">RELATED LINKS</span></span>

[<span data-ttu-id="38a0b-131">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="38a0b-131">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="38a0b-132">Cancelar registro-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="38a0b-132">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


