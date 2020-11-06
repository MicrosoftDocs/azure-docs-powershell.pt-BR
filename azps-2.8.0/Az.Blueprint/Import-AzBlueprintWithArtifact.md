---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 3853cc1785ca0e9f087b1e30870d17d304666df4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597640"
---
# <span data-ttu-id="d3716-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="d3716-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="d3716-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3716-102">SYNOPSIS</span></span>
<span data-ttu-id="d3716-103">Importe um arquivo Blueprint no formato JSON para um objeto Blueprint e salve-o dentro da assinatura especificada ou grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="d3716-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="d3716-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3716-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3716-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d3716-105">DESCRIPTION</span></span>
<span data-ttu-id="d3716-106">Importar uma definição Blueprint com seus artefatos.</span><span class="sxs-lookup"><span data-stu-id="d3716-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="d3716-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3716-107">EXAMPLES</span></span>

### <span data-ttu-id="d3716-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d3716-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="d3716-109">Importar uma definição Blueprint com seus artefatos e salvá-las em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="d3716-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="d3716-110">OS</span><span class="sxs-lookup"><span data-stu-id="d3716-110">PARAMETERS</span></span>

### <span data-ttu-id="d3716-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3716-111">-DefaultProfile</span></span>
<span data-ttu-id="d3716-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3716-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3716-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d3716-113">-Force</span></span>
<span data-ttu-id="d3716-114">Quando definida como true, a execução não solicitará uma confirmação.</span><span class="sxs-lookup"><span data-stu-id="d3716-114">When set to true, execution will not ask for a confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3716-115">-InputPath</span><span class="sxs-lookup"><span data-stu-id="d3716-115">-InputPath</span></span>
<span data-ttu-id="d3716-116">Caminho para um arquivo JSON de Blueprint no disco.</span><span class="sxs-lookup"><span data-stu-id="d3716-116">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="d3716-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="d3716-117">-ManagementGroupId</span></span>
<span data-ttu-id="d3716-118">ID do grupo de gerenciamento em que a definição do plano ou será salva.</span><span class="sxs-lookup"><span data-stu-id="d3716-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3716-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3716-119">-Name</span></span>
<span data-ttu-id="d3716-120">Nome da definição do plano.</span><span class="sxs-lookup"><span data-stu-id="d3716-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="d3716-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d3716-121">-SubscriptionId</span></span>
<span data-ttu-id="d3716-122">ID da assinatura na qual a definição do plano ou será salva.</span><span class="sxs-lookup"><span data-stu-id="d3716-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3716-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3716-123">CommonParameters</span></span>
<span data-ttu-id="d3716-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3716-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d3716-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3716-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3716-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d3716-126">INPUTS</span></span>

### <span data-ttu-id="d3716-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d3716-127">System.String</span></span>

## <span data-ttu-id="d3716-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d3716-128">OUTPUTS</span></span>

### <span data-ttu-id="d3716-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d3716-129">System.String</span></span>

## <span data-ttu-id="d3716-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d3716-130">NOTES</span></span>

## <span data-ttu-id="d3716-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3716-131">RELATED LINKS</span></span>
