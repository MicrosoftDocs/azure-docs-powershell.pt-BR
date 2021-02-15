---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
ms.openlocfilehash: eb5c139aea0520df77bf86af01bc3c02f8118263
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118116"
---
# <span data-ttu-id="050d2-101">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="050d2-101">Remove-AzSearchService</span></span>

## <span data-ttu-id="050d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="050d2-102">SYNOPSIS</span></span>
<span data-ttu-id="050d2-103">Remover um serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="050d2-103">Remove an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="050d2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="050d2-104">SYNTAX</span></span>

### <span data-ttu-id="050d2-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="050d2-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="050d2-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="050d2-106">InputObjectParameterSet</span></span>
```
Remove-AzSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="050d2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="050d2-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchService [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="050d2-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="050d2-108">DESCRIPTION</span></span>
<span data-ttu-id="050d2-109">O **cmdlet Remove-AzSearchService** remove um serviço de Pesquisa Cognitiva do Azure com parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="050d2-109">The **Remove-AzSearchService** cmdlet removes an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="050d2-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="050d2-110">EXAMPLES</span></span>

### <span data-ttu-id="050d2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="050d2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="050d2-112">O exemplo remove um serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="050d2-112">The example removes an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="050d2-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="050d2-113">PARAMETERS</span></span>

### <span data-ttu-id="050d2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="050d2-114">-DefaultProfile</span></span>
<span data-ttu-id="050d2-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="050d2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="050d2-116">-Forçar</span><span class="sxs-lookup"><span data-stu-id="050d2-116">-Force</span></span>
<span data-ttu-id="050d2-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="050d2-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="050d2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="050d2-118">-InputObject</span></span>
<span data-ttu-id="050d2-119">Objeto de entrada do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="050d2-119">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="050d2-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="050d2-120">-Name</span></span>
<span data-ttu-id="050d2-121">Nome do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="050d2-121">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="050d2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="050d2-122">-PassThru</span></span>
<span data-ttu-id="050d2-123">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="050d2-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="050d2-124">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="050d2-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="050d2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="050d2-125">-ResourceGroupName</span></span>
<span data-ttu-id="050d2-126">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="050d2-126">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="050d2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="050d2-127">-ResourceId</span></span>
<span data-ttu-id="050d2-128">ID do Recurso de Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="050d2-128">Azure Cognitive Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="050d2-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="050d2-129">-Confirm</span></span>
<span data-ttu-id="050d2-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="050d2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="050d2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="050d2-131">-WhatIf</span></span>
<span data-ttu-id="050d2-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="050d2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="050d2-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="050d2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="050d2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="050d2-134">CommonParameters</span></span>
<span data-ttu-id="050d2-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="050d2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="050d2-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="050d2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="050d2-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="050d2-137">INPUTS</span></span>

### <span data-ttu-id="050d2-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="050d2-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="050d2-139">System.String</span><span class="sxs-lookup"><span data-stu-id="050d2-139">System.String</span></span>

## <span data-ttu-id="050d2-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="050d2-140">OUTPUTS</span></span>

### <span data-ttu-id="050d2-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="050d2-141">System.Boolean</span></span>

## <span data-ttu-id="050d2-142">Notas</span><span class="sxs-lookup"><span data-stu-id="050d2-142">NOTES</span></span>

## <span data-ttu-id="050d2-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="050d2-143">RELATED LINKS</span></span>

[<span data-ttu-id="050d2-144">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="050d2-144">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="050d2-145">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="050d2-145">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="050d2-146">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="050d2-146">Set-AzSearchService</span></span>](./Set-AzSearchService.md)
