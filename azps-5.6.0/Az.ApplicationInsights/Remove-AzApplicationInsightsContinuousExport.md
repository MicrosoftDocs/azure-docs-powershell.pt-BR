---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: b2ada8c4a58b38eee9ab235bbcd88429934ac00c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885895"
---
# <span data-ttu-id="65ef1-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="65ef1-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="65ef1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65ef1-102">SYNOPSIS</span></span>
<span data-ttu-id="65ef1-103">Remover uma configuração de exportação contínua em um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="65ef1-103">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="65ef1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="65ef1-104">SYNTAX</span></span>

### <span data-ttu-id="65ef1-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="65ef1-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65ef1-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65ef1-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65ef1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65ef1-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65ef1-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="65ef1-108">DESCRIPTION</span></span>
<span data-ttu-id="65ef1-109">Remover uma configuração de exportação contínua em um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="65ef1-109">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="65ef1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65ef1-110">EXAMPLES</span></span>

### <span data-ttu-id="65ef1-111">Exemplo 1 Remover uma configuração de exportação contínua em um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="65ef1-111">Example 1 Remove a continuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="65ef1-112">Remover configuração de exportação contínua de insights de aplicativo com a id de exportação "uGOoki0jQsyEs3IdQ83Q4QsNr4=" para o recurso chamado "test" no grupo de recursos "testgroup"</span><span class="sxs-lookup"><span data-stu-id="65ef1-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="65ef1-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="65ef1-113">PARAMETERS</span></span>

### <span data-ttu-id="65ef1-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="65ef1-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="65ef1-115">Objeto Application Insights Component.</span><span class="sxs-lookup"><span data-stu-id="65ef1-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="65ef1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65ef1-116">-DefaultProfile</span></span>
<span data-ttu-id="65ef1-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="65ef1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65ef1-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="65ef1-118">-ExportId</span></span>
<span data-ttu-id="65ef1-119">ID de Exportação Contínua do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="65ef1-119">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="65ef1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="65ef1-120">-Name</span></span>
<span data-ttu-id="65ef1-121">Nome do componente do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="65ef1-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="65ef1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65ef1-122">-PassThru</span></span>
<span data-ttu-id="65ef1-123">Se especificado, a gravação será true caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="65ef1-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="65ef1-124">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="65ef1-124">This parameter is optional.</span></span> <span data-ttu-id="65ef1-125">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="65ef1-125">Default value is false.</span></span>

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

### <span data-ttu-id="65ef1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65ef1-126">-ResourceGroupName</span></span>
<span data-ttu-id="65ef1-127">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="65ef1-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="65ef1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65ef1-128">-ResourceId</span></span>
<span data-ttu-id="65ef1-129">ID do Recurso de Componente do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="65ef1-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="65ef1-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65ef1-130">-Confirm</span></span>
<span data-ttu-id="65ef1-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65ef1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65ef1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65ef1-132">-WhatIf</span></span>
<span data-ttu-id="65ef1-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="65ef1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65ef1-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="65ef1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65ef1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65ef1-135">CommonParameters</span></span>
<span data-ttu-id="65ef1-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65ef1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65ef1-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65ef1-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65ef1-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65ef1-138">INPUTS</span></span>

### <span data-ttu-id="65ef1-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="65ef1-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="65ef1-140">System.String</span><span class="sxs-lookup"><span data-stu-id="65ef1-140">System.String</span></span>

## <span data-ttu-id="65ef1-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="65ef1-141">OUTPUTS</span></span>

### <span data-ttu-id="65ef1-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="65ef1-142">System.Boolean</span></span>

## <span data-ttu-id="65ef1-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="65ef1-143">NOTES</span></span>

## <span data-ttu-id="65ef1-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65ef1-144">RELATED LINKS</span></span>
