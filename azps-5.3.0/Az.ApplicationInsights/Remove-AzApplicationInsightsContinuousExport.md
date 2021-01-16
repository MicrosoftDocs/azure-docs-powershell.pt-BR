---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 6138d3d454a23cdbdbaa67d7ee668c5ffa752b4a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272048"
---
# <span data-ttu-id="7fd3d-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="7fd3d-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="7fd3d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7fd3d-102">SYNOPSIS</span></span>
<span data-ttu-id="7fd3d-103">Remover uma configuração de exportação contínua em um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="7fd3d-103">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="7fd3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7fd3d-104">SYNTAX</span></span>

### <span data-ttu-id="7fd3d-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7fd3d-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fd3d-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fd3d-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fd3d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fd3d-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fd3d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7fd3d-108">DESCRIPTION</span></span>
<span data-ttu-id="7fd3d-109">Remover uma configuração de exportação contínua em um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="7fd3d-109">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="7fd3d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7fd3d-110">EXAMPLES</span></span>

### <span data-ttu-id="7fd3d-111">Exemplo 1 remover uma configuração de exportação contínua em um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="7fd3d-111">Example 1 Remove a continuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="7fd3d-112">Remover a configuração de exportação contínua do Application insights com a ID de exportação "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" do recurso chamado "teste" no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="7fd3d-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="7fd3d-113">OS</span><span class="sxs-lookup"><span data-stu-id="7fd3d-113">PARAMETERS</span></span>

### <span data-ttu-id="7fd3d-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="7fd3d-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="7fd3d-115">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="7fd3d-115">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fd3d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fd3d-116">-DefaultProfile</span></span>
<span data-ttu-id="7fd3d-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7fd3d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fd3d-118">-Exportid</span><span class="sxs-lookup"><span data-stu-id="7fd3d-118">-ExportId</span></span>
<span data-ttu-id="7fd3d-119">ID de exportação contínua do Application insights.</span><span class="sxs-lookup"><span data-stu-id="7fd3d-119">Application Insights Continuous Export ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd3d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="7fd3d-120">-Name</span></span>
<span data-ttu-id="7fd3d-121">Nome do componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="7fd3d-121">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd3d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7fd3d-122">-PassThru</span></span>
<span data-ttu-id="7fd3d-123">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7fd3d-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="7fd3d-124">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7fd3d-124">This parameter is optional.</span></span> <span data-ttu-id="7fd3d-125">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="7fd3d-125">Default value is false.</span></span>

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

### <span data-ttu-id="7fd3d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fd3d-126">-ResourceGroupName</span></span>
<span data-ttu-id="7fd3d-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7fd3d-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd3d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fd3d-128">-ResourceId</span></span>
<span data-ttu-id="7fd3d-129">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="7fd3d-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="7fd3d-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7fd3d-130">-Confirm</span></span>
<span data-ttu-id="7fd3d-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fd3d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fd3d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fd3d-132">-WhatIf</span></span>
<span data-ttu-id="7fd3d-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7fd3d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fd3d-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7fd3d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fd3d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fd3d-135">CommonParameters</span></span>
<span data-ttu-id="7fd3d-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fd3d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fd3d-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fd3d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fd3d-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7fd3d-138">INPUTS</span></span>

### <span data-ttu-id="7fd3d-139">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="7fd3d-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="7fd3d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7fd3d-140">System.String</span></span>

## <span data-ttu-id="7fd3d-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7fd3d-141">OUTPUTS</span></span>

### <span data-ttu-id="7fd3d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7fd3d-142">System.Boolean</span></span>

## <span data-ttu-id="7fd3d-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7fd3d-143">NOTES</span></span>

## <span data-ttu-id="7fd3d-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7fd3d-144">RELATED LINKS</span></span>
