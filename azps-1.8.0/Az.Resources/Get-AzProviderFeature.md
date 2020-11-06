---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: 46a18d981bae7a8528a866d4f21cf5b07b64732f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599428"
---
# <span data-ttu-id="d6dc2-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="d6dc2-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="d6dc2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="d6dc2-103">Obtém informações sobre os recursos do provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="d6dc2-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="d6dc2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6dc2-104">SYNTAX</span></span>

### <span data-ttu-id="d6dc2-105">ListAvailableParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d6dc2-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6dc2-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="d6dc2-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6dc2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d6dc2-107">DESCRIPTION</span></span>
<span data-ttu-id="d6dc2-108">O cmdlet **Get-AzProviderFeature** Obtém o nome do recurso, o nome do provedor e o status de registro dos recursos do provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="d6dc2-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="d6dc2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6dc2-109">EXAMPLES</span></span>

### <span data-ttu-id="d6dc2-110">Exemplo 1: obter todos os recursos disponíveis</span><span class="sxs-lookup"><span data-stu-id="d6dc2-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="d6dc2-111">Esse comando obtém todos os recursos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d6dc2-111">This command gets all available features.</span></span>

### <span data-ttu-id="d6dc2-112">Exemplo 2: obter informações sobre um recurso específico</span><span class="sxs-lookup"><span data-stu-id="d6dc2-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="d6dc2-113">Esse comando obtém informações para o recurso chamado AllowPreReleaseRegions para o provedor especificado.</span><span class="sxs-lookup"><span data-stu-id="d6dc2-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="d6dc2-114">OS</span><span class="sxs-lookup"><span data-stu-id="d6dc2-114">PARAMETERS</span></span>

### <span data-ttu-id="d6dc2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6dc2-115">-DefaultProfile</span></span>
<span data-ttu-id="d6dc2-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d6dc2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6dc2-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="d6dc2-117">-FeatureName</span></span>
<span data-ttu-id="d6dc2-118">Especifica o nome do recurso a obter.</span><span class="sxs-lookup"><span data-stu-id="d6dc2-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="d6dc2-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="d6dc2-119">-ListAvailable</span></span>
<span data-ttu-id="d6dc2-120">Indica que esse cmdlet obtém todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="d6dc2-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="d6dc2-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="d6dc2-121">-ProviderNamespace</span></span>
<span data-ttu-id="d6dc2-122">Especifica o namespace para o qual este cmdlet obtém recursos do provedor.</span><span class="sxs-lookup"><span data-stu-id="d6dc2-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="d6dc2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6dc2-123">CommonParameters</span></span>
<span data-ttu-id="d6dc2-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6dc2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6dc2-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6dc2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6dc2-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d6dc2-126">INPUTS</span></span>

### <span data-ttu-id="d6dc2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d6dc2-127">System.String</span></span>

## <span data-ttu-id="d6dc2-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d6dc2-128">OUTPUTS</span></span>

### <span data-ttu-id="d6dc2-129">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="d6dc2-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="d6dc2-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d6dc2-130">NOTES</span></span>

## <span data-ttu-id="d6dc2-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6dc2-131">RELATED LINKS</span></span>

[<span data-ttu-id="d6dc2-132">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="d6dc2-132">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)


