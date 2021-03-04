---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: bc1ec66846037a7081af85809f2187b5d35aecb7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893006"
---
# <span data-ttu-id="e8a3d-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="e8a3d-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="e8a3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8a3d-102">SYNOPSIS</span></span>
<span data-ttu-id="e8a3d-103">Publique uma nova versão de um projeto.</span><span class="sxs-lookup"><span data-stu-id="e8a3d-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="e8a3d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e8a3d-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> [-ChangeNote <String>] -Blueprint <PSBlueprint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8a3d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e8a3d-105">DESCRIPTION</span></span>
<span data-ttu-id="e8a3d-106">Publique uma nova versão de uma definição de projeto.</span><span class="sxs-lookup"><span data-stu-id="e8a3d-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="e8a3d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8a3d-107">EXAMPLES</span></span>

### <span data-ttu-id="e8a3d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e8a3d-108">Example 1</span></span>
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

<span data-ttu-id="e8a3d-109">Publique uma nova versão de uma definição de projeto.</span><span class="sxs-lookup"><span data-stu-id="e8a3d-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="e8a3d-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e8a3d-110">PARAMETERS</span></span>

### <span data-ttu-id="e8a3d-111">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="e8a3d-111">-Blueprint</span></span>
<span data-ttu-id="e8a3d-112">Objeto Blueprint.</span><span class="sxs-lookup"><span data-stu-id="e8a3d-112">Blueprint object.</span></span>

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

### <span data-ttu-id="e8a3d-113">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="e8a3d-113">-ChangeNote</span></span>
<span data-ttu-id="e8a3d-114">Observações para descrever o conteúdo desta versão de projeto.</span><span class="sxs-lookup"><span data-stu-id="e8a3d-114">Notes to describe the contents of this blueprint version.</span></span>

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

### <span data-ttu-id="e8a3d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8a3d-115">-DefaultProfile</span></span>
<span data-ttu-id="e8a3d-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e8a3d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8a3d-117">-Version</span><span class="sxs-lookup"><span data-stu-id="e8a3d-117">-Version</span></span>
<span data-ttu-id="e8a3d-118">Versão para a definição do projeto.</span><span class="sxs-lookup"><span data-stu-id="e8a3d-118">Version for the blueprint definition.</span></span>

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

### <span data-ttu-id="e8a3d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8a3d-119">-Confirm</span></span>
<span data-ttu-id="e8a3d-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8a3d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8a3d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8a3d-121">-WhatIf</span></span>
<span data-ttu-id="e8a3d-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e8a3d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8a3d-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e8a3d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8a3d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8a3d-124">CommonParameters</span></span>
<span data-ttu-id="e8a3d-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8a3d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8a3d-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8a3d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8a3d-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8a3d-127">INPUTS</span></span>

### <span data-ttu-id="e8a3d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e8a3d-128">System.String</span></span>

### <span data-ttu-id="e8a3d-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="e8a3d-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="e8a3d-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e8a3d-130">OUTPUTS</span></span>

### <span data-ttu-id="e8a3d-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="e8a3d-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="e8a3d-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="e8a3d-132">NOTES</span></span>

## <span data-ttu-id="e8a3d-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8a3d-133">RELATED LINKS</span></span>
