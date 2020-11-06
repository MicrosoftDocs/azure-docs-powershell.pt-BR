---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
ms.openlocfilehash: 5e4802aff3c887a76cc376cac001ac20d9a98eea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432587"
---
# <span data-ttu-id="ec88b-101">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="ec88b-101">Get-AzureRmProviderFeature</span></span>

## <span data-ttu-id="ec88b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ec88b-102">SYNOPSIS</span></span>
<span data-ttu-id="ec88b-103">Obtém informações sobre os recursos do provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="ec88b-103">Gets information about Azure provider features.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec88b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec88b-104">SYNTAX</span></span>

### <span data-ttu-id="ec88b-105">ListAvailableParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ec88b-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec88b-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="ec88b-106">GetFeature</span></span>
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec88b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ec88b-107">DESCRIPTION</span></span>
<span data-ttu-id="ec88b-108">O cmdlet **Get-AzureRmProviderFeature** Obtém o nome do recurso, o nome do provedor e o status de registro dos recursos do provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="ec88b-108">The **Get-AzureRmProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="ec88b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ec88b-109">EXAMPLES</span></span>

### <span data-ttu-id="ec88b-110">Exemplo 1: obter todos os recursos disponíveis</span><span class="sxs-lookup"><span data-stu-id="ec88b-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzureRmProviderFeature -ListAvailable
```

<span data-ttu-id="ec88b-111">Esse comando obtém todos os recursos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ec88b-111">This command gets all available features.</span></span>

### <span data-ttu-id="ec88b-112">Exemplo 2: obter informações sobre um recurso específico</span><span class="sxs-lookup"><span data-stu-id="ec88b-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="ec88b-113">Esse comando obtém informações para o recurso chamado AllowPreReleaseRegions para o provedor especificado.</span><span class="sxs-lookup"><span data-stu-id="ec88b-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="ec88b-114">OS</span><span class="sxs-lookup"><span data-stu-id="ec88b-114">PARAMETERS</span></span>

### <span data-ttu-id="ec88b-115">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="ec88b-115">-FeatureName</span></span>
<span data-ttu-id="ec88b-116">Especifica o nome do recurso a obter.</span><span class="sxs-lookup"><span data-stu-id="ec88b-116">Specifies the name of the feature to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec88b-117">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="ec88b-117">-ListAvailable</span></span>
<span data-ttu-id="ec88b-118">Indica que esse cmdlet obtém todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="ec88b-118">Indicates that this cmdlet gets all features.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailableParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec88b-119">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="ec88b-119">-ProviderNamespace</span></span>
<span data-ttu-id="ec88b-120">Especifica o namespace para o qual este cmdlet obtém recursos do provedor.</span><span class="sxs-lookup"><span data-stu-id="ec88b-120">Specifies the namespace for which this cmdlet gets provider features.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec88b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec88b-121">-DefaultProfile</span></span>
<span data-ttu-id="ec88b-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ec88b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec88b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec88b-123">CommonParameters</span></span>
<span data-ttu-id="ec88b-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec88b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec88b-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec88b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec88b-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ec88b-126">INPUTS</span></span>

## <span data-ttu-id="ec88b-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ec88b-127">OUTPUTS</span></span>

### <span data-ttu-id="ec88b-128">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSProviderFeature]</span><span class="sxs-lookup"><span data-stu-id="ec88b-128">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="ec88b-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ec88b-129">NOTES</span></span>

## <span data-ttu-id="ec88b-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec88b-130">RELATED LINKS</span></span>

[<span data-ttu-id="ec88b-131">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="ec88b-131">Register-AzureRmProviderFeature</span></span>](./Register-AzureRmProviderFeature.md)


