---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
ms.openlocfilehash: 9b0db1cc72064b502b9961fba73598b94790af1a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111446"
---
# <span data-ttu-id="48d65-101">Export-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="48d65-101">Export-AzTemplateSpec</span></span>

## <span data-ttu-id="48d65-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48d65-102">SYNOPSIS</span></span>
<span data-ttu-id="48d65-103">Exporta uma Especificação de Modelo para o sistema de arquivos local</span><span class="sxs-lookup"><span data-stu-id="48d65-103">Exports a Template Spec to the local filesystem</span></span>

## <span data-ttu-id="48d65-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48d65-104">SYNTAX</span></span>

### <span data-ttu-id="48d65-105">ExportByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="48d65-105">ExportByNameParameterSet (Default)</span></span>
```
Export-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48d65-106">ExportByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48d65-106">ExportByIdParameterSet</span></span>
```
Export-AzTemplateSpec [-ResourceId] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48d65-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="48d65-107">DESCRIPTION</span></span>
<span data-ttu-id="48d65-108">Exporta uma versão específica da Especificação de Modelo para o sistema de arquivos local.</span><span class="sxs-lookup"><span data-stu-id="48d65-108">Exports a specific Template Spec version to the local filesystem.</span></span>

## <span data-ttu-id="48d65-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="48d65-109">EXAMPLES</span></span>

### <span data-ttu-id="48d65-110">Exemplo 1: Exportar por nome</span><span class="sxs-lookup"><span data-stu-id="48d65-110">Example 1: Export by name</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="48d65-111">Exporta a versão 'v1.0' da Especificação de Modelo denominada 'MyTemplateSpec' dentro do grupo de recursos 'myRG' para a pasta de saída local "v1".</span><span class="sxs-lookup"><span data-stu-id="48d65-111">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' to the local output folder "v1".</span></span>

### <span data-ttu-id="48d65-112">Exemplo 2: Exportar por ID de recurso</span><span class="sxs-lookup"><span data-stu-id="48d65-112">Example 2: Export by resource id</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="48d65-113">Exporta a versão 'v1.0' da Especificação de Modelo chamada "MyTemplateSpec" no grupo de recursos "myRG" da subId de assinatura para a pasta de saída \{ \} local "v1".</span><span class="sxs-lookup"><span data-stu-id="48d65-113">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\} to the local output folder "v1".</span></span>

## <span data-ttu-id="48d65-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48d65-114">PARAMETERS</span></span>

### <span data-ttu-id="48d65-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48d65-115">-DefaultProfile</span></span>
<span data-ttu-id="48d65-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48d65-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48d65-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="48d65-117">-Name</span></span>
<span data-ttu-id="48d65-118">O nome da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="48d65-118">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48d65-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="48d65-119">-OutputFolder</span></span>
<span data-ttu-id="48d65-120">O caminho para a pasta para a qual a versão de especificação do modelo será saída.</span><span class="sxs-lookup"><span data-stu-id="48d65-120">The path to the folder where the template spec version will be output to.</span></span>

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

### <span data-ttu-id="48d65-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48d65-121">-ResourceGroupName</span></span>
<span data-ttu-id="48d65-122">O nome do grupo de recursos da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="48d65-122">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48d65-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48d65-123">-ResourceId</span></span>
<span data-ttu-id="48d65-124">A ID de recurso totalmente qualificada da especificação do modelo. Exemplo: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="48d65-124">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48d65-125">-Versão</span><span class="sxs-lookup"><span data-stu-id="48d65-125">-Version</span></span>
<span data-ttu-id="48d65-126">A versão da especificação do modelo a ser exportada.</span><span class="sxs-lookup"><span data-stu-id="48d65-126">The version of the template spec to export.</span></span>

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

### <span data-ttu-id="48d65-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="48d65-127">-Confirm</span></span>
<span data-ttu-id="48d65-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48d65-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48d65-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48d65-129">-WhatIf</span></span>
<span data-ttu-id="48d65-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="48d65-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48d65-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="48d65-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48d65-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48d65-132">CommonParameters</span></span>
<span data-ttu-id="48d65-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48d65-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48d65-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48d65-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48d65-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="48d65-135">INPUTS</span></span>

### <span data-ttu-id="48d65-136">System.String</span><span class="sxs-lookup"><span data-stu-id="48d65-136">System.String</span></span>

## <span data-ttu-id="48d65-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="48d65-137">OUTPUTS</span></span>

### <span data-ttu-id="48d65-138">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="48d65-138">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="48d65-139">Notas</span><span class="sxs-lookup"><span data-stu-id="48d65-139">NOTES</span></span>

## <span data-ttu-id="48d65-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48d65-140">RELATED LINKS</span></span>
