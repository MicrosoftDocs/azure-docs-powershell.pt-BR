---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermproviderfeature
schema: 2.0.0
ms.openlocfilehash: 182accdabc368e72451a0c1d9a1d78f1cf561730
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785860"
---
# <span data-ttu-id="a7543-101">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="a7543-101">Get-AzureRmProviderFeature</span></span>

## <span data-ttu-id="a7543-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7543-102">SYNOPSIS</span></span>
<span data-ttu-id="a7543-103">Obtém informações sobre os recursos do provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="a7543-103">Gets information about Azure provider features.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7543-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7543-104">SYNTAX</span></span>

### <span data-ttu-id="a7543-105">ListAvailableParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a7543-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7543-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="a7543-106">GetFeature</span></span>
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7543-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a7543-107">DESCRIPTION</span></span>
<span data-ttu-id="a7543-108">O cmdlet **Get-AzureRmProviderFeature** Obtém o nome do recurso, o nome do provedor e o status de registro dos recursos do provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="a7543-108">The **Get-AzureRmProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="a7543-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7543-109">EXAMPLES</span></span>

### <span data-ttu-id="a7543-110">Exemplo 1: obter todos os recursos disponíveis</span><span class="sxs-lookup"><span data-stu-id="a7543-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzureRmProviderFeature -ListAvailable
```

<span data-ttu-id="a7543-111">Esse comando obtém todos os recursos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a7543-111">This command gets all available features.</span></span>

### <span data-ttu-id="a7543-112">Exemplo 2: obter informações sobre um recurso específico</span><span class="sxs-lookup"><span data-stu-id="a7543-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="a7543-113">Esse comando obtém informações para o recurso chamado AllowPreReleaseRegions para o provedor especificado.</span><span class="sxs-lookup"><span data-stu-id="a7543-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="a7543-114">OS</span><span class="sxs-lookup"><span data-stu-id="a7543-114">PARAMETERS</span></span>

### <span data-ttu-id="a7543-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7543-115">-DefaultProfile</span></span>
<span data-ttu-id="a7543-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a7543-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7543-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="a7543-117">-FeatureName</span></span>
<span data-ttu-id="a7543-118">Especifica o nome do recurso a obter.</span><span class="sxs-lookup"><span data-stu-id="a7543-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="a7543-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="a7543-119">-ListAvailable</span></span>
<span data-ttu-id="a7543-120">Indica que esse cmdlet obtém todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="a7543-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="a7543-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="a7543-121">-ProviderNamespace</span></span>
<span data-ttu-id="a7543-122">Especifica o namespace para o qual este cmdlet obtém recursos do provedor.</span><span class="sxs-lookup"><span data-stu-id="a7543-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="a7543-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7543-123">CommonParameters</span></span>
<span data-ttu-id="a7543-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7543-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7543-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7543-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7543-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a7543-126">INPUTS</span></span>

## <span data-ttu-id="a7543-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a7543-127">OUTPUTS</span></span>

## <span data-ttu-id="a7543-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a7543-128">NOTES</span></span>

## <span data-ttu-id="a7543-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7543-129">RELATED LINKS</span></span>

[<span data-ttu-id="a7543-130">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="a7543-130">Register-AzureRmProviderFeature</span></span>](./Register-AzureRmProviderFeature.md)


