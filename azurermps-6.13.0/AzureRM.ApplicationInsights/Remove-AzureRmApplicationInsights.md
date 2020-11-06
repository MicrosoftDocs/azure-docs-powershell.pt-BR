---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
ms.openlocfilehash: 72a5affb91cbd2c1dfbe78cc7ee86da799b6ae50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426481"
---
# <span data-ttu-id="545b2-101">Remove-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="545b2-101">Remove-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="545b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="545b2-102">SYNOPSIS</span></span>
<span data-ttu-id="545b2-103">Remover um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="545b2-103">Remove an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="545b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="545b2-104">SYNTAX</span></span>

### <span data-ttu-id="545b2-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="545b2-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="545b2-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="545b2-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="545b2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="545b2-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="545b2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="545b2-108">DESCRIPTION</span></span>
<span data-ttu-id="545b2-109">Remover um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="545b2-109">Remove an application insights resource</span></span>

## <span data-ttu-id="545b2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="545b2-110">EXAMPLES</span></span>

### <span data-ttu-id="545b2-111">Exemplo 1 remover um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="545b2-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="545b2-112">Remover um recurso do applciation insights chamado "Test" no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="545b2-112">Remove an applciation insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="545b2-113">OS</span><span class="sxs-lookup"><span data-stu-id="545b2-113">PARAMETERS</span></span>

### <span data-ttu-id="545b2-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="545b2-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="545b2-115">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="545b2-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="545b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="545b2-116">-DefaultProfile</span></span>
<span data-ttu-id="545b2-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="545b2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545b2-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="545b2-118">-Name</span></span>
<span data-ttu-id="545b2-119">Nome do componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="545b2-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="545b2-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="545b2-120">-PassThru</span></span>
<span data-ttu-id="545b2-121">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="545b2-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="545b2-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="545b2-122">This parameter is optional.</span></span> <span data-ttu-id="545b2-123">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="545b2-123">Default value is false.</span></span>

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

### <span data-ttu-id="545b2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="545b2-124">-ResourceGroupName</span></span>
<span data-ttu-id="545b2-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="545b2-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="545b2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="545b2-126">-ResourceId</span></span>
<span data-ttu-id="545b2-127">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="545b2-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="545b2-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="545b2-128">-Confirm</span></span>
<span data-ttu-id="545b2-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="545b2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="545b2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="545b2-130">-WhatIf</span></span>
<span data-ttu-id="545b2-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="545b2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="545b2-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="545b2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="545b2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="545b2-133">CommonParameters</span></span>
<span data-ttu-id="545b2-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="545b2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="545b2-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="545b2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="545b2-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="545b2-136">INPUTS</span></span>

### <span data-ttu-id="545b2-137">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="545b2-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="545b2-138">Parâmetros: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="545b2-138">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="545b2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="545b2-139">System.String</span></span>

## <span data-ttu-id="545b2-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="545b2-140">OUTPUTS</span></span>

### <span data-ttu-id="545b2-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="545b2-141">System.Boolean</span></span>

## <span data-ttu-id="545b2-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="545b2-142">NOTES</span></span>

## <span data-ttu-id="545b2-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="545b2-143">RELATED LINKS</span></span>
