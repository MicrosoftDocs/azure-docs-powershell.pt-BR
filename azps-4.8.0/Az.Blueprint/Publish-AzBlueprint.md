---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: 32b59902bca68496c3a6c9e1656ac618824b9f38
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947896"
---
# <span data-ttu-id="e4876-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="e4876-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="e4876-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4876-102">SYNOPSIS</span></span>
<span data-ttu-id="e4876-103">Publicar uma nova versão de um plano.</span><span class="sxs-lookup"><span data-stu-id="e4876-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="e4876-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4876-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> [-ChangeNote <String>] -Blueprint <PSBlueprint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4876-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4876-105">DESCRIPTION</span></span>
<span data-ttu-id="e4876-106">Publicar uma nova versão de uma definição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="e4876-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="e4876-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4876-107">EXAMPLES</span></span>

### <span data-ttu-id="e4876-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e4876-108">Example 1</span></span>
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

<span data-ttu-id="e4876-109">Publicar uma nova versão de uma definição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="e4876-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="e4876-110">OS</span><span class="sxs-lookup"><span data-stu-id="e4876-110">PARAMETERS</span></span>

### <span data-ttu-id="e4876-111">-Plano gráfico</span><span class="sxs-lookup"><span data-stu-id="e4876-111">-Blueprint</span></span>
<span data-ttu-id="e4876-112">Objeto Blueprint.</span><span class="sxs-lookup"><span data-stu-id="e4876-112">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4876-113">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="e4876-113">-ChangeNote</span></span>
<span data-ttu-id="e4876-114">Observações para descrever o conteúdo da versão Blueprint.</span><span class="sxs-lookup"><span data-stu-id="e4876-114">Notes to describe the contents of this blueprint version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4876-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4876-115">-DefaultProfile</span></span>
<span data-ttu-id="e4876-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4876-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4876-117">-Versão</span><span class="sxs-lookup"><span data-stu-id="e4876-117">-Version</span></span>
<span data-ttu-id="e4876-118">Versão para a definição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="e4876-118">Version for the blueprint definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4876-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e4876-119">-Confirm</span></span>
<span data-ttu-id="e4876-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4876-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4876-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4876-121">-WhatIf</span></span>
<span data-ttu-id="e4876-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e4876-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4876-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4876-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4876-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4876-124">CommonParameters</span></span>
<span data-ttu-id="e4876-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4876-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4876-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4876-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4876-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4876-127">INPUTS</span></span>

### <span data-ttu-id="e4876-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e4876-128">System.String</span></span>

### <span data-ttu-id="e4876-129">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="e4876-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="e4876-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4876-130">OUTPUTS</span></span>

### <span data-ttu-id="e4876-131">Microsoft. Azure. Commands. Blueprint. Models. PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="e4876-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="e4876-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4876-132">NOTES</span></span>

## <span data-ttu-id="e4876-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4876-133">RELATED LINKS</span></span>
