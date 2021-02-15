---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: f14da4760f70c8e4ba95136b81a884f830f4f44a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111424"
---
# <span data-ttu-id="cbb4f-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="cbb4f-101">Get-AzLocation</span></span>

## <span data-ttu-id="cbb4f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cbb4f-102">SYNOPSIS</span></span>
<span data-ttu-id="cbb4f-103">Obtém todos os locais e os provedores de recursos com suporte para cada local.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="cbb4f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbb4f-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbb4f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="cbb4f-105">DESCRIPTION</span></span>
<span data-ttu-id="cbb4f-106">O **cmdlet Get-AzLocation** obtém todos os locais e os provedores de recursos com suporte para cada local.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="cbb4f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cbb4f-107">EXAMPLES</span></span>

### <span data-ttu-id="cbb4f-108">Exemplo 1: Obter todos os locais e os provedores de recursos com suporte</span><span class="sxs-lookup"><span data-stu-id="cbb4f-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="cbb4f-109">Esse comando obtém todos os locais e os provedores de recursos com suporte para cada local.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="cbb4f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbb4f-110">PARAMETERS</span></span>

### <span data-ttu-id="cbb4f-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cbb4f-111">-ApiVersion</span></span>
<span data-ttu-id="cbb4f-112">Especifica a versão da API com suporte do Provedor de Recursos.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="cbb4f-113">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="cbb4f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbb4f-114">-DefaultProfile</span></span>
<span data-ttu-id="cbb4f-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="cbb4f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbb4f-116">-Pré-</span><span class="sxs-lookup"><span data-stu-id="cbb4f-116">-Pre</span></span>
<span data-ttu-id="cbb4f-117">Indica que esse cmdlet considera as versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="cbb4f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbb4f-118">CommonParameters</span></span>
<span data-ttu-id="cbb4f-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbb4f-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbb4f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbb4f-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="cbb4f-121">INPUTS</span></span>

### <span data-ttu-id="cbb4f-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cbb4f-122">None</span></span>

## <span data-ttu-id="cbb4f-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="cbb4f-123">OUTPUTS</span></span>

### <span data-ttu-id="cbb4f-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span><span class="sxs-lookup"><span data-stu-id="cbb4f-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span></span>

## <span data-ttu-id="cbb4f-125">Notas</span><span class="sxs-lookup"><span data-stu-id="cbb4f-125">NOTES</span></span>

## <span data-ttu-id="cbb4f-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbb4f-126">RELATED LINKS</span></span>
