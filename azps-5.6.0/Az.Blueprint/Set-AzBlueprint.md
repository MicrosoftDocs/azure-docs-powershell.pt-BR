---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/set-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
ms.openlocfilehash: 5511be0e20c99a6a120e2f7591287b9ee17b0943
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887023"
---
# <span data-ttu-id="8d57d-101">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="8d57d-101">Set-AzBlueprint</span></span>

## <span data-ttu-id="8d57d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d57d-102">SYNOPSIS</span></span>
<span data-ttu-id="8d57d-103">Atualize uma definição de projeto.</span><span class="sxs-lookup"><span data-stu-id="8d57d-103">Update a blueprint definition.</span></span>

## <span data-ttu-id="8d57d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8d57d-104">SYNTAX</span></span>

### <span data-ttu-id="8d57d-105">UpdateBlueprintBySubscription (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8d57d-105">UpdateBlueprintBySubscription (Default)</span></span>
```
Set-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d57d-106">UpdateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="8d57d-106">UpdateBlueprintByManagementGroup</span></span>
```
Set-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d57d-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8d57d-107">DESCRIPTION</span></span>
<span data-ttu-id="8d57d-108">Atualize uma definição de projeto e salve-a no grupo de gerenciamento ou assinatura especificado.</span><span class="sxs-lookup"><span data-stu-id="8d57d-108">Update a blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="8d57d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d57d-109">EXAMPLES</span></span>

### <span data-ttu-id="8d57d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8d57d-110">Example 1</span></span>
```powershell
PS C:\> Set-AzBlueprint -Name MyBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -BlueprintFile C:\Blueprint.json

Name              : SimpleBlueprint
Id                : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint
ManagementGroupId : myManagementGroupId
Versions          : 
Description       : test
TimeCreated       : 2019-05-12
TargetScope       : Subscription
Parameters        : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue}
ResourceGroups    : {AppNetworkRG}
```

<span data-ttu-id="8d57d-111">Atualize uma definição de projeto com novos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8d57d-111">Update a blueprint definition with new parameters.</span></span>

## <span data-ttu-id="8d57d-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8d57d-112">PARAMETERS</span></span>

### <span data-ttu-id="8d57d-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="8d57d-113">-BlueprintFile</span></span>
<span data-ttu-id="8d57d-114">Caminho para um arquivo JSON de esquema no disco.</span><span class="sxs-lookup"><span data-stu-id="8d57d-114">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="8d57d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d57d-115">-DefaultProfile</span></span>
<span data-ttu-id="8d57d-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d57d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d57d-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="8d57d-117">-ManagementGroupId</span></span>
<span data-ttu-id="8d57d-118">ID do Grupo de Gerenciamento onde a definição de projeto é ou será salva.</span><span class="sxs-lookup"><span data-stu-id="8d57d-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d57d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8d57d-119">-Name</span></span>
<span data-ttu-id="8d57d-120">Nome da definição de projeto.</span><span class="sxs-lookup"><span data-stu-id="8d57d-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="8d57d-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d57d-121">-SubscriptionId</span></span>
<span data-ttu-id="8d57d-122">ID da assinatura onde a definição de projeto é ou será salva.</span><span class="sxs-lookup"><span data-stu-id="8d57d-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d57d-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d57d-123">-Confirm</span></span>
<span data-ttu-id="8d57d-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d57d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d57d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d57d-125">-WhatIf</span></span>
<span data-ttu-id="8d57d-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8d57d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d57d-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8d57d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d57d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d57d-128">CommonParameters</span></span>
<span data-ttu-id="8d57d-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d57d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d57d-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d57d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d57d-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d57d-131">INPUTS</span></span>

### <span data-ttu-id="8d57d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="8d57d-132">System.String</span></span>

## <span data-ttu-id="8d57d-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8d57d-133">OUTPUTS</span></span>

### <span data-ttu-id="8d57d-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="8d57d-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="8d57d-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="8d57d-135">NOTES</span></span>

## <span data-ttu-id="8d57d-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d57d-136">RELATED LINKS</span></span>
