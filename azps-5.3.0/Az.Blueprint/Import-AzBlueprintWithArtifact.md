---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 43877ecb7fe7e90f0619a26a54eea534ac1390b3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434468"
---
# <span data-ttu-id="b76e7-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="b76e7-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="b76e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b76e7-102">SYNOPSIS</span></span>
<span data-ttu-id="b76e7-103">Importe um arquivo Blueprint no formato JSON para um objeto Blueprint e salve-o dentro da assinatura especificada ou grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="b76e7-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="b76e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b76e7-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-IncludeSubFolders] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b76e7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b76e7-105">DESCRIPTION</span></span>
<span data-ttu-id="b76e7-106">Importar uma definição Blueprint com seus artefatos.</span><span class="sxs-lookup"><span data-stu-id="b76e7-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="b76e7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b76e7-107">EXAMPLES</span></span>

### <span data-ttu-id="b76e7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b76e7-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="b76e7-109">Importar uma definição Blueprint com seus artefatos e salvá-las em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="b76e7-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="b76e7-110">OS</span><span class="sxs-lookup"><span data-stu-id="b76e7-110">PARAMETERS</span></span>

### <span data-ttu-id="b76e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b76e7-111">-DefaultProfile</span></span>
<span data-ttu-id="b76e7-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b76e7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b76e7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b76e7-113">-Force</span></span>
<span data-ttu-id="b76e7-114">Quando definida como true, a execução não solicitará uma confirmação.</span><span class="sxs-lookup"><span data-stu-id="b76e7-114">When set to true, execution will not ask for a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b76e7-115">-IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="b76e7-115">-IncludeSubFolders</span></span>
<span data-ttu-id="b76e7-116">Quando definido como verdadeiro, o artefato nas subpastas será incluído.</span><span class="sxs-lookup"><span data-stu-id="b76e7-116">When set to true, artifact in the subfolders will be included.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b76e7-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="b76e7-117">-InputPath</span></span>
<span data-ttu-id="b76e7-118">Caminho para um arquivo JSON de Blueprint no disco.</span><span class="sxs-lookup"><span data-stu-id="b76e7-118">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="b76e7-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="b76e7-119">-ManagementGroupId</span></span>
<span data-ttu-id="b76e7-120">ID do grupo de gerenciamento em que a definição do plano ou será salva.</span><span class="sxs-lookup"><span data-stu-id="b76e7-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="b76e7-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b76e7-121">-Name</span></span>
<span data-ttu-id="b76e7-122">Nome da definição do plano.</span><span class="sxs-lookup"><span data-stu-id="b76e7-122">Blueprint definition name.</span></span>

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

### <span data-ttu-id="b76e7-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b76e7-123">-PassThru</span></span>
<span data-ttu-id="b76e7-124">Quando definido, o cmdlet retornará um objeto que representa a definição Blueprint importada.</span><span class="sxs-lookup"><span data-stu-id="b76e7-124">When set, the cmdlet will return an object representing the imported blueprint definition.</span></span> <span data-ttu-id="b76e7-125">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="b76e7-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b76e7-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b76e7-126">-SubscriptionId</span></span>
<span data-ttu-id="b76e7-127">ID da assinatura na qual a definição do plano ou será salva.</span><span class="sxs-lookup"><span data-stu-id="b76e7-127">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="b76e7-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b76e7-128">-Confirm</span></span>
<span data-ttu-id="b76e7-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b76e7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b76e7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b76e7-130">-WhatIf</span></span>
<span data-ttu-id="b76e7-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b76e7-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b76e7-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b76e7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b76e7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b76e7-133">CommonParameters</span></span>
<span data-ttu-id="b76e7-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b76e7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b76e7-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b76e7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b76e7-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b76e7-136">INPUTS</span></span>

### <span data-ttu-id="b76e7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b76e7-137">System.String</span></span>

## <span data-ttu-id="b76e7-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b76e7-138">OUTPUTS</span></span>

### <span data-ttu-id="b76e7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b76e7-139">System.String</span></span>

## <span data-ttu-id="b76e7-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b76e7-140">NOTES</span></span>

## <span data-ttu-id="b76e7-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b76e7-141">RELATED LINKS</span></span>
