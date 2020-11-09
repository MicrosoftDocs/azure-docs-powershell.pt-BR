---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
ms.openlocfilehash: 9b0db1cc72064b502b9961fba73598b94790af1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281742"
---
# <span data-ttu-id="f52a0-101">Export-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="f52a0-101">Export-AzTemplateSpec</span></span>

## <span data-ttu-id="f52a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f52a0-102">SYNOPSIS</span></span>
<span data-ttu-id="f52a0-103">Exporta uma especificação de modelo para o sistema de arquivos local</span><span class="sxs-lookup"><span data-stu-id="f52a0-103">Exports a Template Spec to the local filesystem</span></span>

## <span data-ttu-id="f52a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f52a0-104">SYNTAX</span></span>

### <span data-ttu-id="f52a0-105">ExportByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f52a0-105">ExportByNameParameterSet (Default)</span></span>
```
Export-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f52a0-106">ExportByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f52a0-106">ExportByIdParameterSet</span></span>
```
Export-AzTemplateSpec [-ResourceId] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f52a0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f52a0-107">DESCRIPTION</span></span>
<span data-ttu-id="f52a0-108">Exporta uma versão de especificação de modelo específica para o sistema de arquivos local.</span><span class="sxs-lookup"><span data-stu-id="f52a0-108">Exports a specific Template Spec version to the local filesystem.</span></span>

## <span data-ttu-id="f52a0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f52a0-109">EXAMPLES</span></span>

### <span data-ttu-id="f52a0-110">Exemplo 1: exportar por nome</span><span class="sxs-lookup"><span data-stu-id="f52a0-110">Example 1: Export by name</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="f52a0-111">Exporta a versão "v 1.0" da especificação do modelo chamada "MyTemplateSpec" no grupo de recursos "myRG" para a pasta de saída local "v1".</span><span class="sxs-lookup"><span data-stu-id="f52a0-111">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' to the local output folder "v1".</span></span>

### <span data-ttu-id="f52a0-112">Exemplo 2: exportar por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="f52a0-112">Example 2: Export by resource id</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="f52a0-113">Exporta a versão "v 1.0" da especificação do modelo chamada "MyTemplateSpec" no grupo de recursos "myRG" da assinatura \{ subId \} para a pasta de saída local "v1".</span><span class="sxs-lookup"><span data-stu-id="f52a0-113">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\} to the local output folder "v1".</span></span>

## <span data-ttu-id="f52a0-114">OS</span><span class="sxs-lookup"><span data-stu-id="f52a0-114">PARAMETERS</span></span>

### <span data-ttu-id="f52a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f52a0-115">-DefaultProfile</span></span>
<span data-ttu-id="f52a0-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f52a0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f52a0-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f52a0-117">-Name</span></span>
<span data-ttu-id="f52a0-118">O nome da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="f52a0-118">The name of the template spec.</span></span>

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

### <span data-ttu-id="f52a0-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="f52a0-119">-OutputFolder</span></span>
<span data-ttu-id="f52a0-120">O caminho para a pasta em que a versão de especificação do modelo será impressa.</span><span class="sxs-lookup"><span data-stu-id="f52a0-120">The path to the folder where the template spec version will be output to.</span></span>

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

### <span data-ttu-id="f52a0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f52a0-121">-ResourceGroupName</span></span>
<span data-ttu-id="f52a0-122">O nome do grupo de recursos de especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="f52a0-122">The name of the template spec's resource group.</span></span>

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

### <span data-ttu-id="f52a0-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f52a0-123">-ResourceId</span></span>
<span data-ttu-id="f52a0-124">A ID de recurso totalmente qualificado da especificação do modelo. exemplo:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="f52a0-124">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="f52a0-125">-Versão</span><span class="sxs-lookup"><span data-stu-id="f52a0-125">-Version</span></span>
<span data-ttu-id="f52a0-126">A versão da especificação do modelo a ser exportada.</span><span class="sxs-lookup"><span data-stu-id="f52a0-126">The version of the template spec to export.</span></span>

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

### <span data-ttu-id="f52a0-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f52a0-127">-Confirm</span></span>
<span data-ttu-id="f52a0-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f52a0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f52a0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f52a0-129">-WhatIf</span></span>
<span data-ttu-id="f52a0-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f52a0-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f52a0-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f52a0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f52a0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f52a0-132">CommonParameters</span></span>
<span data-ttu-id="f52a0-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f52a0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f52a0-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f52a0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f52a0-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f52a0-135">INPUTS</span></span>

### <span data-ttu-id="f52a0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f52a0-136">System.String</span></span>

## <span data-ttu-id="f52a0-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f52a0-137">OUTPUTS</span></span>

### <span data-ttu-id="f52a0-138">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f52a0-138">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f52a0-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f52a0-139">NOTES</span></span>

## <span data-ttu-id="f52a0-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f52a0-140">RELATED LINKS</span></span>
