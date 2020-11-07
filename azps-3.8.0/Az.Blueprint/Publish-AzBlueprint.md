---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: e61beaa43f881aa148401ef91cd4cb37c1f18d88
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940991"
---
# <span data-ttu-id="f0519-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="f0519-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="f0519-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f0519-102">SYNOPSIS</span></span>
<span data-ttu-id="f0519-103">Publicar uma nova versão de um plano.</span><span class="sxs-lookup"><span data-stu-id="f0519-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="f0519-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0519-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> -ChangeNote <String> -Blueprint <PSBlueprint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0519-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f0519-105">DESCRIPTION</span></span>
<span data-ttu-id="f0519-106">Publicar uma nova versão de uma definição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="f0519-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="f0519-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f0519-107">EXAMPLES</span></span>

### <span data-ttu-id="f0519-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f0519-108">Example 1</span></span>
```powershell
PS C:\> Publish-AzBlueprint -Blueprint $bp -Version 1.0 

Name           : SimpleBlueprint
Id             : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/versions/1.0
SubscriptionId : 00000000-1111-0000-1111-000000000000
Version        : 1.0
Description    : My simple blueprint
TimeCreated    : 2019-05-30
TargetScope    : Subscription
Parameters     : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroups : {storageRG}
```
<span data-ttu-id="f0519-109">Publicar uma nova versão de uma definição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="f0519-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="f0519-110">OS</span><span class="sxs-lookup"><span data-stu-id="f0519-110">PARAMETERS</span></span>

### <span data-ttu-id="f0519-111">-Plano gráfico</span><span class="sxs-lookup"><span data-stu-id="f0519-111">-Blueprint</span></span>
<span data-ttu-id="f0519-112">Objeto Blueprint.</span><span class="sxs-lookup"><span data-stu-id="f0519-112">Blueprint object.</span></span>

```yaml
Type: PSBlueprint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0519-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0519-113">-DefaultProfile</span></span>
<span data-ttu-id="f0519-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f0519-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0519-115">-Versão</span><span class="sxs-lookup"><span data-stu-id="f0519-115">-Version</span></span>
<span data-ttu-id="f0519-116">Versão para a definição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="f0519-116">Version for the blueprint definition.</span></span>

### <span data-ttu-id="f0519-117">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="f0519-117">-ChangeNote</span></span>
<span data-ttu-id="f0519-118">Observações para descrever o conteúdo da versão Blueprint.</span><span class="sxs-lookup"><span data-stu-id="f0519-118">Notes to describe the contents of this blueprint version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0519-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0519-119">CommonParameters</span></span>
<span data-ttu-id="f0519-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0519-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f0519-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0519-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0519-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f0519-122">INPUTS</span></span>

### <span data-ttu-id="f0519-123">System. String</span><span class="sxs-lookup"><span data-stu-id="f0519-123">System.String</span></span>

### <span data-ttu-id="f0519-124">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="f0519-124">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="f0519-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f0519-125">OUTPUTS</span></span>

### <span data-ttu-id="f0519-126">Microsoft. Azure. Commands. Blueprint. Models. PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="f0519-126">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="f0519-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f0519-127">NOTES</span></span>

## <span data-ttu-id="f0519-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0519-128">RELATED LINKS</span></span>
