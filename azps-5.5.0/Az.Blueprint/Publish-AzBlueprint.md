---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: 32b59902bca68496c3a6c9e1656ac618824b9f38
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116943"
---
# <span data-ttu-id="c0ac1-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="c0ac1-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="c0ac1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="c0ac1-103">Publicar uma nova versão de um diagrama.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="c0ac1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0ac1-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> [-ChangeNote <String>] -Blueprint <PSBlueprint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0ac1-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c0ac1-105">DESCRIPTION</span></span>
<span data-ttu-id="c0ac1-106">Publicar uma nova versão de uma definição de plano de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="c0ac1-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c0ac1-107">EXAMPLES</span></span>

### <span data-ttu-id="c0ac1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c0ac1-108">Example 1</span></span>
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

<span data-ttu-id="c0ac1-109">Publicar uma nova versão de uma definição de plano de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="c0ac1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0ac1-110">PARAMETERS</span></span>

### <span data-ttu-id="c0ac1-111">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="c0ac1-111">-Blueprint</span></span>
<span data-ttu-id="c0ac1-112">Objeto de planta.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-112">Blueprint object.</span></span>

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

### <span data-ttu-id="c0ac1-113">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="c0ac1-113">-ChangeNote</span></span>
<span data-ttu-id="c0ac1-114">Anotações para descrever o conteúdo desta versão de diagrama.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-114">Notes to describe the contents of this blueprint version.</span></span>

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

### <span data-ttu-id="c0ac1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0ac1-115">-DefaultProfile</span></span>
<span data-ttu-id="c0ac1-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0ac1-117">-Versão</span><span class="sxs-lookup"><span data-stu-id="c0ac1-117">-Version</span></span>
<span data-ttu-id="c0ac1-118">Versão para a definição de diagrama.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-118">Version for the blueprint definition.</span></span>

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

### <span data-ttu-id="c0ac1-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c0ac1-119">-Confirm</span></span>
<span data-ttu-id="c0ac1-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0ac1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0ac1-121">-WhatIf</span></span>
<span data-ttu-id="c0ac1-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0ac1-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0ac1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0ac1-124">CommonParameters</span></span>
<span data-ttu-id="c0ac1-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0ac1-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0ac1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0ac1-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="c0ac1-127">INPUTS</span></span>

### <span data-ttu-id="c0ac1-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c0ac1-128">System.String</span></span>

### <span data-ttu-id="c0ac1-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="c0ac1-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="c0ac1-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="c0ac1-130">OUTPUTS</span></span>

### <span data-ttu-id="c0ac1-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="c0ac1-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="c0ac1-132">Notas</span><span class="sxs-lookup"><span data-stu-id="c0ac1-132">NOTES</span></span>

## <span data-ttu-id="c0ac1-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0ac1-133">RELATED LINKS</span></span>
