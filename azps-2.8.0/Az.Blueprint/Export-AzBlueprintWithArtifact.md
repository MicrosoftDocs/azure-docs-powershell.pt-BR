---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 2c349d99e8a3529d4f1423a43bd31ab2500664c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597652"
---
# <span data-ttu-id="81c47-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="81c47-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="81c47-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81c47-102">SYNOPSIS</span></span>
<span data-ttu-id="81c47-103">Exportar a definição Blueprint especificada para o local de saída especificado como um arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="81c47-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="81c47-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81c47-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81c47-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81c47-105">DESCRIPTION</span></span>
<span data-ttu-id="81c47-106">Exporte uma definição Blueprint com seus artefatos e salve em disco.</span><span class="sxs-lookup"><span data-stu-id="81c47-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="81c47-107">Esse cmdlet exporta a versão mais recente (rascunho ou publicado) da planta.</span><span class="sxs-lookup"><span data-stu-id="81c47-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="81c47-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81c47-108">EXAMPLES</span></span>

### <span data-ttu-id="81c47-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="81c47-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="81c47-110">Exporte uma definição Blueprint com seus artefatos e salve em disco.</span><span class="sxs-lookup"><span data-stu-id="81c47-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="81c47-111">OS</span><span class="sxs-lookup"><span data-stu-id="81c47-111">PARAMETERS</span></span>

### <span data-ttu-id="81c47-112">-Plano gráfico</span><span class="sxs-lookup"><span data-stu-id="81c47-112">-Blueprint</span></span>
<span data-ttu-id="81c47-113">O objeto de definição Blueprint a ser exportado.</span><span class="sxs-lookup"><span data-stu-id="81c47-113">The blueprint definition object to export.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81c47-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81c47-114">-DefaultProfile</span></span>
<span data-ttu-id="81c47-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81c47-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81c47-116">-Force</span><span class="sxs-lookup"><span data-stu-id="81c47-116">-Force</span></span>
<span data-ttu-id="81c47-117">Quando definida como true, a execução não solicitará uma confirmação.</span><span class="sxs-lookup"><span data-stu-id="81c47-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="81c47-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="81c47-118">-OutputPath</span></span>
<span data-ttu-id="81c47-119">Caminho para um arquivo no disco onde exportar a definição Blueprint no formato JSON.</span><span class="sxs-lookup"><span data-stu-id="81c47-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="81c47-120">-Versão</span><span class="sxs-lookup"><span data-stu-id="81c47-120">-Version</span></span>
<span data-ttu-id="81c47-121">Versão de definição de esquema publicada.</span><span class="sxs-lookup"><span data-stu-id="81c47-121">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="81c47-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c47-122">CommonParameters</span></span>
<span data-ttu-id="81c47-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81c47-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="81c47-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81c47-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c47-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81c47-125">INPUTS</span></span>

### <span data-ttu-id="81c47-126">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="81c47-126">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="81c47-127">System. String</span><span class="sxs-lookup"><span data-stu-id="81c47-127">System.String</span></span>

## <span data-ttu-id="81c47-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81c47-128">OUTPUTS</span></span>

### <span data-ttu-id="81c47-129">System. String</span><span class="sxs-lookup"><span data-stu-id="81c47-129">System.String</span></span>

## <span data-ttu-id="81c47-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81c47-130">NOTES</span></span>

## <span data-ttu-id="81c47-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81c47-131">RELATED LINKS</span></span>
