---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 0265a273cb575d2cc3a165afae8f7a2090499cdc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601655"
---
# <span data-ttu-id="ff47e-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="ff47e-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="ff47e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff47e-102">SYNOPSIS</span></span>
<span data-ttu-id="ff47e-103">Remover uma configuração de exportação cotinuous em um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="ff47e-103">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="ff47e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff47e-104">SYNTAX</span></span>

### <span data-ttu-id="ff47e-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ff47e-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff47e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff47e-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff47e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff47e-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff47e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff47e-108">DESCRIPTION</span></span>
<span data-ttu-id="ff47e-109">Remover uma configuração de exportação cotinuous em um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="ff47e-109">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="ff47e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff47e-110">EXAMPLES</span></span>

### <span data-ttu-id="ff47e-111">Exemplo 1 remover uma configuração de exportação cotinuous em um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="ff47e-111">Example 1 Remove a cotinuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="ff47e-112">Remover a configuração de exportação contínua do Application insights com a ID de exportação "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" do recurso chamado "teste" no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="ff47e-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="ff47e-113">OS</span><span class="sxs-lookup"><span data-stu-id="ff47e-113">PARAMETERS</span></span>

### <span data-ttu-id="ff47e-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ff47e-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="ff47e-115">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="ff47e-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="ff47e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff47e-116">-DefaultProfile</span></span>
<span data-ttu-id="ff47e-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ff47e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff47e-118">-Exportid</span><span class="sxs-lookup"><span data-stu-id="ff47e-118">-ExportId</span></span>
<span data-ttu-id="ff47e-119">ID de exportação contínua do Application insights.</span><span class="sxs-lookup"><span data-stu-id="ff47e-119">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="ff47e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff47e-120">-Name</span></span>
<span data-ttu-id="ff47e-121">Nome do componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="ff47e-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="ff47e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff47e-122">-PassThru</span></span>
<span data-ttu-id="ff47e-123">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ff47e-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="ff47e-124">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ff47e-124">This parameter is optional.</span></span> <span data-ttu-id="ff47e-125">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="ff47e-125">Default value is false.</span></span>

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

### <span data-ttu-id="ff47e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff47e-126">-ResourceGroupName</span></span>
<span data-ttu-id="ff47e-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ff47e-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="ff47e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff47e-128">-ResourceId</span></span>
<span data-ttu-id="ff47e-129">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="ff47e-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="ff47e-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ff47e-130">-Confirm</span></span>
<span data-ttu-id="ff47e-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff47e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff47e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff47e-132">-WhatIf</span></span>
<span data-ttu-id="ff47e-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ff47e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff47e-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ff47e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff47e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff47e-135">CommonParameters</span></span>
<span data-ttu-id="ff47e-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff47e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff47e-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff47e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff47e-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff47e-138">INPUTS</span></span>

### <span data-ttu-id="ff47e-139">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ff47e-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="ff47e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ff47e-140">System.String</span></span>

## <span data-ttu-id="ff47e-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff47e-141">OUTPUTS</span></span>

### <span data-ttu-id="ff47e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ff47e-142">System.Boolean</span></span>

## <span data-ttu-id="ff47e-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff47e-143">NOTES</span></span>

## <span data-ttu-id="ff47e-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff47e-144">RELATED LINKS</span></span>
