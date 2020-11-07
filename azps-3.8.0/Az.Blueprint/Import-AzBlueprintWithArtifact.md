---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 7a1778ce107e9753f78876aff3a2dfba19e138e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943686"
---
# <span data-ttu-id="bfc24-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="bfc24-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="bfc24-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bfc24-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc24-103">Importe um arquivo Blueprint no formato JSON para um objeto Blueprint e salve-o dentro da assinatura especificada ou grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="bfc24-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="bfc24-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bfc24-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfc24-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bfc24-105">DESCRIPTION</span></span>
<span data-ttu-id="bfc24-106">Importar uma definição Blueprint com seus artefatos.</span><span class="sxs-lookup"><span data-stu-id="bfc24-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="bfc24-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfc24-107">EXAMPLES</span></span>

### <span data-ttu-id="bfc24-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bfc24-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="bfc24-109">Importar uma definição Blueprint com seus artefatos e salvá-las em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="bfc24-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="bfc24-110">OS</span><span class="sxs-lookup"><span data-stu-id="bfc24-110">PARAMETERS</span></span>

### <span data-ttu-id="bfc24-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfc24-111">-DefaultProfile</span></span>
<span data-ttu-id="bfc24-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bfc24-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfc24-113">-Force</span><span class="sxs-lookup"><span data-stu-id="bfc24-113">-Force</span></span>
<span data-ttu-id="bfc24-114">Quando definida como true, a execução não solicitará uma confirmação.</span><span class="sxs-lookup"><span data-stu-id="bfc24-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="bfc24-115">-IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="bfc24-115">-IncludeSubFolders</span></span>
<span data-ttu-id="bfc24-116">Quando definido como verdadeiro, o artefato nas subpastas será incluído.</span><span class="sxs-lookup"><span data-stu-id="bfc24-116">When set to true, artifact in the subfolders will be included.</span></span>

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

### <span data-ttu-id="bfc24-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="bfc24-117">-InputPath</span></span>
<span data-ttu-id="bfc24-118">Caminho para um arquivo JSON de Blueprint no disco.</span><span class="sxs-lookup"><span data-stu-id="bfc24-118">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="bfc24-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="bfc24-119">-ManagementGroupId</span></span>
<span data-ttu-id="bfc24-120">ID do grupo de gerenciamento em que a definição do plano ou será salva.</span><span class="sxs-lookup"><span data-stu-id="bfc24-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="bfc24-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="bfc24-121">-Name</span></span>
<span data-ttu-id="bfc24-122">Nome da definição do plano.</span><span class="sxs-lookup"><span data-stu-id="bfc24-122">Blueprint definition name.</span></span>

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

### <span data-ttu-id="bfc24-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bfc24-123">-SubscriptionId</span></span>
<span data-ttu-id="bfc24-124">ID da assinatura na qual a definição do plano ou será salva.</span><span class="sxs-lookup"><span data-stu-id="bfc24-124">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="bfc24-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc24-125">CommonParameters</span></span>
<span data-ttu-id="bfc24-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfc24-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bfc24-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfc24-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc24-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bfc24-128">INPUTS</span></span>

### <span data-ttu-id="bfc24-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bfc24-129">System.String</span></span>

## <span data-ttu-id="bfc24-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bfc24-130">OUTPUTS</span></span>

### <span data-ttu-id="bfc24-131">System. String</span><span class="sxs-lookup"><span data-stu-id="bfc24-131">System.String</span></span>

## <span data-ttu-id="bfc24-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bfc24-132">NOTES</span></span>

## <span data-ttu-id="bfc24-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfc24-133">RELATED LINKS</span></span>
