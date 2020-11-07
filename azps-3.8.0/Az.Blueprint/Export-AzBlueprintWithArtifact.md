---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 2136a224a5d187951b77c6f48e0b610b48b021b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942378"
---
# <span data-ttu-id="1dd17-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="1dd17-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="1dd17-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1dd17-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd17-103">Exportar a definição Blueprint especificada para o local de saída especificado como um arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="1dd17-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="1dd17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1dd17-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dd17-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1dd17-105">DESCRIPTION</span></span>
<span data-ttu-id="1dd17-106">Exporte uma definição Blueprint com seus artefatos e salve em disco.</span><span class="sxs-lookup"><span data-stu-id="1dd17-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="1dd17-107">Esse cmdlet exporta a versão mais recente (rascunho ou publicado) da planta.</span><span class="sxs-lookup"><span data-stu-id="1dd17-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="1dd17-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1dd17-108">EXAMPLES</span></span>

### <span data-ttu-id="1dd17-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1dd17-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="1dd17-110">Exporte uma definição Blueprint com seus artefatos e salve em disco.</span><span class="sxs-lookup"><span data-stu-id="1dd17-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="1dd17-111">OS</span><span class="sxs-lookup"><span data-stu-id="1dd17-111">PARAMETERS</span></span>

### <span data-ttu-id="1dd17-112">-Plano gráfico</span><span class="sxs-lookup"><span data-stu-id="1dd17-112">-Blueprint</span></span>
<span data-ttu-id="1dd17-113">O objeto de definição Blueprint a ser exportado.</span><span class="sxs-lookup"><span data-stu-id="1dd17-113">The blueprint definition object to export.</span></span>

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

### <span data-ttu-id="1dd17-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dd17-114">-DefaultProfile</span></span>
<span data-ttu-id="1dd17-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1dd17-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dd17-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1dd17-116">-Force</span></span>
<span data-ttu-id="1dd17-117">Quando definida como true, a execução não solicitará uma confirmação.</span><span class="sxs-lookup"><span data-stu-id="1dd17-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="1dd17-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="1dd17-118">-OutputPath</span></span>
<span data-ttu-id="1dd17-119">Caminho para um arquivo no disco onde exportar a definição Blueprint no formato JSON.</span><span class="sxs-lookup"><span data-stu-id="1dd17-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="1dd17-120">-Versão</span><span class="sxs-lookup"><span data-stu-id="1dd17-120">-Version</span></span>
<span data-ttu-id="1dd17-121">Versão de definição de esquema publicada.</span><span class="sxs-lookup"><span data-stu-id="1dd17-121">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="1dd17-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd17-122">CommonParameters</span></span>
<span data-ttu-id="1dd17-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dd17-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1dd17-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dd17-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd17-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1dd17-125">INPUTS</span></span>

### <span data-ttu-id="1dd17-126">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="1dd17-126">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="1dd17-127">System. String</span><span class="sxs-lookup"><span data-stu-id="1dd17-127">System.String</span></span>

## <span data-ttu-id="1dd17-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1dd17-128">OUTPUTS</span></span>

### <span data-ttu-id="1dd17-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1dd17-129">System.String</span></span>

## <span data-ttu-id="1dd17-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1dd17-130">NOTES</span></span>

## <span data-ttu-id="1dd17-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1dd17-131">RELATED LINKS</span></span>
