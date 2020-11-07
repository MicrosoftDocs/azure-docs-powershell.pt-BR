---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
ms.openlocfilehash: 11a2aeffc1ab3bb170b2e8543d9fd5d0300e3ce5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941171"
---
# <span data-ttu-id="716b6-101">New-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="716b6-101">New-AzBlueprint</span></span>

## <span data-ttu-id="716b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="716b6-102">SYNOPSIS</span></span>
<span data-ttu-id="716b6-103">Crie uma nova definição Blueprint e salve-a dentro da assinatura especificada ou grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="716b6-103">Create a new blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="716b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="716b6-104">SYNTAX</span></span>

### <span data-ttu-id="716b6-105">CreateBlueprintBySubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="716b6-105">CreateBlueprintBySubscription (Default)</span></span>
```
New-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="716b6-106">CreateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="716b6-106">CreateBlueprintByManagementGroup</span></span>
```
New-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="716b6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="716b6-107">DESCRIPTION</span></span>
<span data-ttu-id="716b6-108">Crie uma nova definição de esquema.</span><span class="sxs-lookup"><span data-stu-id="716b6-108">Create a new blueprint definition.</span></span> 

## <span data-ttu-id="716b6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="716b6-109">EXAMPLES</span></span>

### <span data-ttu-id="716b6-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="716b6-110">Example 1</span></span>
```powershell
PS C:\> New-AzBlueprint -Name MyNewBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -BlueprintFile C:\Blueprint.json

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

<span data-ttu-id="716b6-111">Criar uma nova definição Blueprint dentro da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="716b6-111">Create a new blueprint definition within the specified subscription.</span></span>

## <span data-ttu-id="716b6-112">OS</span><span class="sxs-lookup"><span data-stu-id="716b6-112">PARAMETERS</span></span>

### <span data-ttu-id="716b6-113">-Blueprintfile</span><span class="sxs-lookup"><span data-stu-id="716b6-113">-BlueprintFile</span></span>
<span data-ttu-id="716b6-114">Caminho para um arquivo JSON de Blueprint no disco.</span><span class="sxs-lookup"><span data-stu-id="716b6-114">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="716b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="716b6-115">-DefaultProfile</span></span>
<span data-ttu-id="716b6-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="716b6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="716b6-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="716b6-117">-ManagementGroupId</span></span>
<span data-ttu-id="716b6-118">ID do grupo de gerenciamento em que a definição do plano ou será salva.</span><span class="sxs-lookup"><span data-stu-id="716b6-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="716b6-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="716b6-119">-Name</span></span>
<span data-ttu-id="716b6-120">Nome da definição do plano.</span><span class="sxs-lookup"><span data-stu-id="716b6-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="716b6-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="716b6-121">-SubscriptionId</span></span>
<span data-ttu-id="716b6-122">ID da assinatura na qual a definição do plano ou será salva.</span><span class="sxs-lookup"><span data-stu-id="716b6-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="716b6-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="716b6-123">-Confirm</span></span>
<span data-ttu-id="716b6-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="716b6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="716b6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="716b6-125">-WhatIf</span></span>
<span data-ttu-id="716b6-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="716b6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="716b6-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="716b6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="716b6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="716b6-128">CommonParameters</span></span>
<span data-ttu-id="716b6-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="716b6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="716b6-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="716b6-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="716b6-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="716b6-131">INPUTS</span></span>

### <span data-ttu-id="716b6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="716b6-132">System.String</span></span>

## <span data-ttu-id="716b6-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="716b6-133">OUTPUTS</span></span>

### <span data-ttu-id="716b6-134">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="716b6-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="716b6-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="716b6-135">NOTES</span></span>

## <span data-ttu-id="716b6-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="716b6-136">RELATED LINKS</span></span>
