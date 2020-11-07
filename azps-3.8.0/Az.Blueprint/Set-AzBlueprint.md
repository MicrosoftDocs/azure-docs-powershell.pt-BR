---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
ms.openlocfilehash: 155bf1a7851f6cc8e3283c66297df811738edd2d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940988"
---
# <span data-ttu-id="02507-101">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="02507-101">Set-AzBlueprint</span></span>

## <span data-ttu-id="02507-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02507-102">SYNOPSIS</span></span>
<span data-ttu-id="02507-103">Atualize uma definição de plano.</span><span class="sxs-lookup"><span data-stu-id="02507-103">Update a blueprint definition.</span></span>

## <span data-ttu-id="02507-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02507-104">SYNTAX</span></span>

### <span data-ttu-id="02507-105">UpdateBlueprintBySubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="02507-105">UpdateBlueprintBySubscription (Default)</span></span>
```
Set-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02507-106">UpdateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="02507-106">UpdateBlueprintByManagementGroup</span></span>
```
Set-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02507-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02507-107">DESCRIPTION</span></span>
<span data-ttu-id="02507-108">Atualize uma definição Blueprint e salve-a na assinatura ou no grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="02507-108">Update a blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="02507-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02507-109">EXAMPLES</span></span>

### <span data-ttu-id="02507-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="02507-110">Example 1</span></span>
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

<span data-ttu-id="02507-111">Atualize uma definição Blueprint com novos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="02507-111">Update a blueprint definition with new parameters.</span></span>

## <span data-ttu-id="02507-112">OS</span><span class="sxs-lookup"><span data-stu-id="02507-112">PARAMETERS</span></span>

### <span data-ttu-id="02507-113">-Blueprintfile</span><span class="sxs-lookup"><span data-stu-id="02507-113">-BlueprintFile</span></span>
<span data-ttu-id="02507-114">Caminho para um arquivo JSON de Blueprint no disco.</span><span class="sxs-lookup"><span data-stu-id="02507-114">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription, CreateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02507-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02507-115">-DefaultProfile</span></span>
<span data-ttu-id="02507-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02507-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02507-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="02507-117">-ManagementGroupId</span></span>
<span data-ttu-id="02507-118">ID do grupo de gerenciamento em que a definição do plano ou será salva.</span><span class="sxs-lookup"><span data-stu-id="02507-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintByManagementGroup, ManagementGroupScope, ByManagementGroupAndName, ByManagementGroupNameAndVersion, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02507-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="02507-119">-Name</span></span>
<span data-ttu-id="02507-120">Nome da definição do plano.</span><span class="sxs-lookup"><span data-stu-id="02507-120">Blueprint definition name.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription, CreateBlueprintByManagementGroup, ImportBlueprint
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02507-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="02507-121">-SubscriptionId</span></span>
<span data-ttu-id="02507-122">ID da assinatura na qual a definição do plano ou será salva.</span><span class="sxs-lookup"><span data-stu-id="02507-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription, ImportBlueprint, SubscriptionScope, BySubscriptionAndName, BySubscriptionNameAndVersion, BySubscriptionNameAndLatestPublished
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02507-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="02507-123">-Confirm</span></span>
<span data-ttu-id="02507-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02507-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02507-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02507-125">-WhatIf</span></span>
<span data-ttu-id="02507-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="02507-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02507-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="02507-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02507-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02507-128">CommonParameters</span></span>
<span data-ttu-id="02507-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02507-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="02507-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02507-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02507-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02507-131">INPUTS</span></span>

### <span data-ttu-id="02507-132">System. String</span><span class="sxs-lookup"><span data-stu-id="02507-132">System.String</span></span>

## <span data-ttu-id="02507-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02507-133">OUTPUTS</span></span>

### <span data-ttu-id="02507-134">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="02507-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="02507-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02507-135">NOTES</span></span>

## <span data-ttu-id="02507-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02507-136">RELATED LINKS</span></span>
