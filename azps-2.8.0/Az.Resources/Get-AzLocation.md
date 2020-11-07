---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: 17bc16b38bc967f9997b22d7dd86b056253d8a18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773366"
---
# <span data-ttu-id="02c1a-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="02c1a-101">Get-AzLocation</span></span>

## <span data-ttu-id="02c1a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="02c1a-103">Obtém todos os locais e os provedores de recursos com suporte para cada local.</span><span class="sxs-lookup"><span data-stu-id="02c1a-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="02c1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02c1a-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02c1a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02c1a-105">DESCRIPTION</span></span>
<span data-ttu-id="02c1a-106">O cmdlet **Get-AzLocation** Obtém todos os locais e os provedores de recursos com suporte para cada local.</span><span class="sxs-lookup"><span data-stu-id="02c1a-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="02c1a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02c1a-107">EXAMPLES</span></span>

### <span data-ttu-id="02c1a-108">Exemplo 1: obter todos os locais e os provedores de recursos com suporte</span><span class="sxs-lookup"><span data-stu-id="02c1a-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="02c1a-109">Esse comando obtém todos os locais e os provedores de recursos com suporte para cada local.</span><span class="sxs-lookup"><span data-stu-id="02c1a-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="02c1a-110">OS</span><span class="sxs-lookup"><span data-stu-id="02c1a-110">PARAMETERS</span></span>

### <span data-ttu-id="02c1a-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="02c1a-111">-ApiVersion</span></span>
<span data-ttu-id="02c1a-112">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="02c1a-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="02c1a-113">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="02c1a-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="02c1a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c1a-114">-DefaultProfile</span></span>
<span data-ttu-id="02c1a-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="02c1a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02c1a-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="02c1a-116">-Pre</span></span>
<span data-ttu-id="02c1a-117">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="02c1a-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="02c1a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c1a-118">CommonParameters</span></span>
<span data-ttu-id="02c1a-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02c1a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c1a-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02c1a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c1a-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02c1a-121">INPUTS</span></span>

### <span data-ttu-id="02c1a-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="02c1a-122">None</span></span>

## <span data-ttu-id="02c1a-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02c1a-123">OUTPUTS</span></span>

### <span data-ttu-id="02c1a-124">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceProviderLocation</span><span class="sxs-lookup"><span data-stu-id="02c1a-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span></span>

## <span data-ttu-id="02c1a-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02c1a-125">NOTES</span></span>

## <span data-ttu-id="02c1a-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02c1a-126">RELATED LINKS</span></span>
