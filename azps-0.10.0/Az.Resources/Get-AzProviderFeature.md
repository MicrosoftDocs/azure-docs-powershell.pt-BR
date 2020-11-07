---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: 1296e1e135acce9d4840e625d96931f6ecc11625
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776439"
---
# <span data-ttu-id="4b694-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="4b694-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="4b694-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b694-102">SYNOPSIS</span></span>
<span data-ttu-id="4b694-103">Obtém informações sobre os recursos do provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="4b694-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="4b694-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b694-104">SYNTAX</span></span>

### <span data-ttu-id="4b694-105">ListAvailableParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4b694-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b694-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="4b694-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b694-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b694-107">DESCRIPTION</span></span>
<span data-ttu-id="4b694-108">O cmdlet **Get-AzProviderFeature** Obtém o nome do recurso, o nome do provedor e o status de registro dos recursos do provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="4b694-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="4b694-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b694-109">EXAMPLES</span></span>

### <span data-ttu-id="4b694-110">Exemplo 1: obter todos os recursos disponíveis</span><span class="sxs-lookup"><span data-stu-id="4b694-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="4b694-111">Esse comando obtém todos os recursos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4b694-111">This command gets all available features.</span></span>

### <span data-ttu-id="4b694-112">Exemplo 2: obter informações sobre um recurso específico</span><span class="sxs-lookup"><span data-stu-id="4b694-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="4b694-113">Esse comando obtém informações para o recurso chamado AllowPreReleaseRegions para o provedor especificado.</span><span class="sxs-lookup"><span data-stu-id="4b694-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="4b694-114">OS</span><span class="sxs-lookup"><span data-stu-id="4b694-114">PARAMETERS</span></span>

### <span data-ttu-id="4b694-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b694-115">-DefaultProfile</span></span>
<span data-ttu-id="4b694-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4b694-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b694-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="4b694-117">-FeatureName</span></span>
<span data-ttu-id="4b694-118">Especifica o nome do recurso a obter.</span><span class="sxs-lookup"><span data-stu-id="4b694-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="4b694-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="4b694-119">-ListAvailable</span></span>
<span data-ttu-id="4b694-120">Indica que esse cmdlet obtém todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="4b694-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="4b694-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="4b694-121">-ProviderNamespace</span></span>
<span data-ttu-id="4b694-122">Especifica o namespace para o qual este cmdlet obtém recursos do provedor.</span><span class="sxs-lookup"><span data-stu-id="4b694-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="4b694-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b694-123">CommonParameters</span></span>
<span data-ttu-id="4b694-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b694-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b694-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b694-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b694-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b694-126">INPUTS</span></span>

## <span data-ttu-id="4b694-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b694-127">OUTPUTS</span></span>

## <span data-ttu-id="4b694-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b694-128">NOTES</span></span>

## <span data-ttu-id="4b694-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b694-129">RELATED LINKS</span></span>

[<span data-ttu-id="4b694-130">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="4b694-130">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)

