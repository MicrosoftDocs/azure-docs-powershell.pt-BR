---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: ccccfe4ba17fe9d5fc9f35f6604f5f7bb9263d14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432980"
---
# <span data-ttu-id="b0e33-101">Remove-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="b0e33-101">Remove-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="b0e33-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0e33-102">SYNOPSIS</span></span>
<span data-ttu-id="b0e33-103">Remover uma configuração de exportação cotinuous em um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="b0e33-103">Remove a cotinuous export configuration in an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0e33-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0e33-104">SYNTAX</span></span>

### <span data-ttu-id="b0e33-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b0e33-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0e33-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0e33-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport
 [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0e33-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0e33-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0e33-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0e33-108">DESCRIPTION</span></span>
<span data-ttu-id="b0e33-109">Remover uma configuração de exportação cotinuous em um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="b0e33-109">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="b0e33-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0e33-110">EXAMPLES</span></span>

### <span data-ttu-id="b0e33-111">Exemplo 1 remover uma configuração de exportação cotinuous em um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="b0e33-111">Example 1 Remove a cotinuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="b0e33-112">Remover a configuração de exportação contínua do Application insights com a ID de exportação "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" do recurso chamado "teste" no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="b0e33-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="b0e33-113">OS</span><span class="sxs-lookup"><span data-stu-id="b0e33-113">PARAMETERS</span></span>

### <span data-ttu-id="b0e33-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="b0e33-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="b0e33-115">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="b0e33-115">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0e33-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b0e33-116">-Confirm</span></span>
<span data-ttu-id="b0e33-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0e33-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e33-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0e33-118">-DefaultProfile</span></span>
<span data-ttu-id="b0e33-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0e33-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e33-120">-Exportid</span><span class="sxs-lookup"><span data-stu-id="b0e33-120">-ExportId</span></span>
<span data-ttu-id="b0e33-121">ID de exportação contínua do Application insights.</span><span class="sxs-lookup"><span data-stu-id="b0e33-121">Application Insights Continuous Export ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e33-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0e33-122">-Name</span></span>
<span data-ttu-id="b0e33-123">Nome do componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="b0e33-123">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e33-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0e33-124">-PassThru</span></span>
<span data-ttu-id="b0e33-125">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b0e33-125">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="b0e33-126">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b0e33-126">This parameter is optional.</span></span> <span data-ttu-id="b0e33-127">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="b0e33-127">Default value is false.</span></span>

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

### <span data-ttu-id="b0e33-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0e33-128">-ResourceGroupName</span></span>
<span data-ttu-id="b0e33-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0e33-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e33-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0e33-130">-ResourceId</span></span>
<span data-ttu-id="b0e33-131">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="b0e33-131">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0e33-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0e33-132">-WhatIf</span></span>
<span data-ttu-id="b0e33-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b0e33-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0e33-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b0e33-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e33-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0e33-135">CommonParameters</span></span>
<span data-ttu-id="b0e33-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0e33-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0e33-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0e33-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0e33-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0e33-138">INPUTS</span></span>

### <span data-ttu-id="b0e33-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b0e33-139">System.String</span></span>

## <span data-ttu-id="b0e33-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0e33-140">OUTPUTS</span></span>

### <span data-ttu-id="b0e33-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="b0e33-141">System.Object</span></span>

## <span data-ttu-id="b0e33-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0e33-142">NOTES</span></span>

## <span data-ttu-id="b0e33-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0e33-143">RELATED LINKS</span></span>

