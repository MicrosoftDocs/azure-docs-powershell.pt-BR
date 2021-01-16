---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
ms.openlocfilehash: cbfd316b459c9cd2e1fc60e4416e50c426a3dc19
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262244"
---
# <span data-ttu-id="152ad-101">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="152ad-101">Set-AzBlueprint</span></span>

## <span data-ttu-id="152ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="152ad-102">SYNOPSIS</span></span>
<span data-ttu-id="152ad-103">Atualize uma definição de plano.</span><span class="sxs-lookup"><span data-stu-id="152ad-103">Update a blueprint definition.</span></span>

## <span data-ttu-id="152ad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="152ad-104">SYNTAX</span></span>

### <span data-ttu-id="152ad-105">UpdateBlueprintBySubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="152ad-105">UpdateBlueprintBySubscription (Default)</span></span>
```
Set-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="152ad-106">UpdateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="152ad-106">UpdateBlueprintByManagementGroup</span></span>
```
Set-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="152ad-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="152ad-107">DESCRIPTION</span></span>
<span data-ttu-id="152ad-108">Atualize uma definição Blueprint e salve-a na assinatura ou no grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="152ad-108">Update a blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="152ad-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="152ad-109">EXAMPLES</span></span>

### <span data-ttu-id="152ad-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="152ad-110">Example 1</span></span>
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

<span data-ttu-id="152ad-111">Atualize uma definição Blueprint com novos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="152ad-111">Update a blueprint definition with new parameters.</span></span>

## <span data-ttu-id="152ad-112">OS</span><span class="sxs-lookup"><span data-stu-id="152ad-112">PARAMETERS</span></span>

### <span data-ttu-id="152ad-113">-Blueprintfile</span><span class="sxs-lookup"><span data-stu-id="152ad-113">-BlueprintFile</span></span>
<span data-ttu-id="152ad-114">Caminho para um arquivo JSON de Blueprint no disco.</span><span class="sxs-lookup"><span data-stu-id="152ad-114">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="152ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="152ad-115">-DefaultProfile</span></span>
<span data-ttu-id="152ad-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="152ad-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="152ad-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="152ad-117">-ManagementGroupId</span></span>
<span data-ttu-id="152ad-118">ID do grupo de gerenciamento em que a definição do plano ou será salva.</span><span class="sxs-lookup"><span data-stu-id="152ad-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="152ad-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="152ad-119">-Name</span></span>
<span data-ttu-id="152ad-120">Nome da definição do plano.</span><span class="sxs-lookup"><span data-stu-id="152ad-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="152ad-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="152ad-121">-SubscriptionId</span></span>
<span data-ttu-id="152ad-122">ID da assinatura na qual a definição do plano ou será salva.</span><span class="sxs-lookup"><span data-stu-id="152ad-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="152ad-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="152ad-123">-Confirm</span></span>
<span data-ttu-id="152ad-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="152ad-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="152ad-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="152ad-125">-WhatIf</span></span>
<span data-ttu-id="152ad-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="152ad-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="152ad-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="152ad-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="152ad-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="152ad-128">CommonParameters</span></span>
<span data-ttu-id="152ad-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="152ad-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="152ad-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="152ad-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="152ad-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="152ad-131">INPUTS</span></span>

### <span data-ttu-id="152ad-132">System. String</span><span class="sxs-lookup"><span data-stu-id="152ad-132">System.String</span></span>

## <span data-ttu-id="152ad-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="152ad-133">OUTPUTS</span></span>

### <span data-ttu-id="152ad-134">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="152ad-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="152ad-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="152ad-135">NOTES</span></span>

## <span data-ttu-id="152ad-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="152ad-136">RELATED LINKS</span></span>
