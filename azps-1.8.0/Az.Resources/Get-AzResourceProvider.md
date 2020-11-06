---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
ms.openlocfilehash: 76a0164a5cf4c4d67ecb7f64667b9b87d9bc252c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599413"
---
# <span data-ttu-id="8801b-101">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="8801b-101">Get-AzResourceProvider</span></span>

## <span data-ttu-id="8801b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8801b-102">SYNOPSIS</span></span>
<span data-ttu-id="8801b-103">Obtém um provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="8801b-103">Gets a resource provider.</span></span>

## <span data-ttu-id="8801b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8801b-104">SYNTAX</span></span>

### <span data-ttu-id="8801b-105">ListAvailable (padrão)</span><span class="sxs-lookup"><span data-stu-id="8801b-105">ListAvailable (Default)</span></span>
```
Get-AzResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8801b-106">Indivíduo</span><span class="sxs-lookup"><span data-stu-id="8801b-106">IndividualProvider</span></span>
```
Get-AzResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8801b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8801b-107">DESCRIPTION</span></span>
<span data-ttu-id="8801b-108">O cmdlet **Get-AzResourceProvider** Obtém um provedor de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="8801b-108">The **Get-AzResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="8801b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8801b-109">EXAMPLES</span></span>

## <span data-ttu-id="8801b-110">OS</span><span class="sxs-lookup"><span data-stu-id="8801b-110">PARAMETERS</span></span>

### <span data-ttu-id="8801b-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8801b-111">-ApiVersion</span></span>
<span data-ttu-id="8801b-112">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="8801b-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="8801b-113">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="8801b-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="8801b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8801b-114">-DefaultProfile</span></span>
<span data-ttu-id="8801b-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8801b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8801b-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="8801b-116">-ListAvailable</span></span>
<span data-ttu-id="8801b-117">Indica que essa operação obtém todos os provedores de recursos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="8801b-117">Indicates that this operation gets all available resource providers.</span></span>

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

### <span data-ttu-id="8801b-118">-Local</span><span class="sxs-lookup"><span data-stu-id="8801b-118">-Location</span></span>
<span data-ttu-id="8801b-119">Especifica o local do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="8801b-119">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="8801b-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="8801b-120">-Pre</span></span>
<span data-ttu-id="8801b-121">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="8801b-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8801b-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="8801b-122">-ProviderNamespace</span></span>
<span data-ttu-id="8801b-123">Especifica o namespace do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="8801b-123">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="8801b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8801b-124">CommonParameters</span></span>
<span data-ttu-id="8801b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8801b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8801b-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8801b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8801b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8801b-127">INPUTS</span></span>

### <span data-ttu-id="8801b-128">System. String []</span><span class="sxs-lookup"><span data-stu-id="8801b-128">System.String[]</span></span>

## <span data-ttu-id="8801b-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8801b-129">OUTPUTS</span></span>

### <span data-ttu-id="8801b-130">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="8801b-130">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="8801b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8801b-131">NOTES</span></span>

## <span data-ttu-id="8801b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8801b-132">RELATED LINKS</span></span>

[<span data-ttu-id="8801b-133">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="8801b-133">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

[<span data-ttu-id="8801b-134">Cancelar registro-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="8801b-134">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


