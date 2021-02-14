---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
ms.openlocfilehash: cbfd316b459c9cd2e1fc60e4416e50c426a3dc19
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116942"
---
# <span data-ttu-id="5f2db-101">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="5f2db-101">Set-AzBlueprint</span></span>

## <span data-ttu-id="5f2db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f2db-102">SYNOPSIS</span></span>
<span data-ttu-id="5f2db-103">Atualizar uma definição de planta.</span><span class="sxs-lookup"><span data-stu-id="5f2db-103">Update a blueprint definition.</span></span>

## <span data-ttu-id="5f2db-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f2db-104">SYNTAX</span></span>

### <span data-ttu-id="5f2db-105">UpdateBlueprintBySubscription (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5f2db-105">UpdateBlueprintBySubscription (Default)</span></span>
```
Set-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f2db-106">UpdateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5f2db-106">UpdateBlueprintByManagementGroup</span></span>
```
Set-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f2db-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f2db-107">DESCRIPTION</span></span>
<span data-ttu-id="5f2db-108">Atualize uma definição de plano de trabalho e salve-a no grupo de gerenciamento ou assinatura especificado.</span><span class="sxs-lookup"><span data-stu-id="5f2db-108">Update a blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="5f2db-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5f2db-109">EXAMPLES</span></span>

### <span data-ttu-id="5f2db-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5f2db-110">Example 1</span></span>
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

<span data-ttu-id="5f2db-111">Atualize uma definição de planta com novos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5f2db-111">Update a blueprint definition with new parameters.</span></span>

## <span data-ttu-id="5f2db-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f2db-112">PARAMETERS</span></span>

### <span data-ttu-id="5f2db-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="5f2db-113">-BlueprintFile</span></span>
<span data-ttu-id="5f2db-114">Caminho para um arquivo JSON de esquema no disco.</span><span class="sxs-lookup"><span data-stu-id="5f2db-114">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="5f2db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f2db-115">-DefaultProfile</span></span>
<span data-ttu-id="5f2db-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5f2db-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f2db-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="5f2db-117">-ManagementGroupId</span></span>
<span data-ttu-id="5f2db-118">ID do Grupo de Gerenciamento onde a definição de plano é ou será salva.</span><span class="sxs-lookup"><span data-stu-id="5f2db-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="5f2db-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f2db-119">-Name</span></span>
<span data-ttu-id="5f2db-120">Nome da definição de planta.</span><span class="sxs-lookup"><span data-stu-id="5f2db-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="5f2db-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5f2db-121">-SubscriptionId</span></span>
<span data-ttu-id="5f2db-122">ID da assinatura onde a definição do plano é ou será salva.</span><span class="sxs-lookup"><span data-stu-id="5f2db-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="5f2db-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5f2db-123">-Confirm</span></span>
<span data-ttu-id="5f2db-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f2db-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f2db-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f2db-125">-WhatIf</span></span>
<span data-ttu-id="5f2db-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5f2db-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f2db-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5f2db-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f2db-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f2db-128">CommonParameters</span></span>
<span data-ttu-id="5f2db-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f2db-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f2db-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f2db-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f2db-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="5f2db-131">INPUTS</span></span>

### <span data-ttu-id="5f2db-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5f2db-132">System.String</span></span>

## <span data-ttu-id="5f2db-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="5f2db-133">OUTPUTS</span></span>

### <span data-ttu-id="5f2db-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="5f2db-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="5f2db-135">Notas</span><span class="sxs-lookup"><span data-stu-id="5f2db-135">NOTES</span></span>

## <span data-ttu-id="5f2db-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f2db-136">RELATED LINKS</span></span>
