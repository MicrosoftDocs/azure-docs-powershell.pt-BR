---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: 089561268233876976598f3cf74cd0a52fef8402
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892258"
---
# <span data-ttu-id="eaef6-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="eaef6-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="eaef6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaef6-102">SYNOPSIS</span></span>
<span data-ttu-id="eaef6-103">Remover um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="eaef6-103">Remove an application insights resource</span></span>

## <span data-ttu-id="eaef6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="eaef6-104">SYNTAX</span></span>

### <span data-ttu-id="eaef6-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="eaef6-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eaef6-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaef6-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eaef6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaef6-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaef6-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="eaef6-108">DESCRIPTION</span></span>
<span data-ttu-id="eaef6-109">Remover um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="eaef6-109">Remove an application insights resource</span></span>

## <span data-ttu-id="eaef6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eaef6-110">EXAMPLES</span></span>

### <span data-ttu-id="eaef6-111">Exemplo 1 Remover um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="eaef6-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="eaef6-112">Remover um recurso de insights de aplicativo chamado "test" no grupo de recursos "testgroup"</span><span class="sxs-lookup"><span data-stu-id="eaef6-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="eaef6-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="eaef6-113">PARAMETERS</span></span>

### <span data-ttu-id="eaef6-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="eaef6-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="eaef6-115">Objeto Application Insights Component.</span><span class="sxs-lookup"><span data-stu-id="eaef6-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="eaef6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaef6-116">-DefaultProfile</span></span>
<span data-ttu-id="eaef6-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="eaef6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaef6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="eaef6-118">-Name</span></span>
<span data-ttu-id="eaef6-119">Nome do componente do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="eaef6-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="eaef6-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eaef6-120">-PassThru</span></span>
<span data-ttu-id="eaef6-121">Se especificado, a gravação será true caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="eaef6-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="eaef6-122">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="eaef6-122">This parameter is optional.</span></span> <span data-ttu-id="eaef6-123">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="eaef6-123">Default value is false.</span></span>

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

### <span data-ttu-id="eaef6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaef6-124">-ResourceGroupName</span></span>
<span data-ttu-id="eaef6-125">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="eaef6-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="eaef6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eaef6-126">-ResourceId</span></span>
<span data-ttu-id="eaef6-127">ID do Recurso de Componente do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="eaef6-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="eaef6-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eaef6-128">-Confirm</span></span>
<span data-ttu-id="eaef6-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eaef6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaef6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaef6-130">-WhatIf</span></span>
<span data-ttu-id="eaef6-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="eaef6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaef6-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eaef6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaef6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaef6-133">CommonParameters</span></span>
<span data-ttu-id="eaef6-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaef6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaef6-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eaef6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaef6-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eaef6-136">INPUTS</span></span>

### <span data-ttu-id="eaef6-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="eaef6-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="eaef6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="eaef6-138">System.String</span></span>

## <span data-ttu-id="eaef6-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="eaef6-139">OUTPUTS</span></span>

### <span data-ttu-id="eaef6-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eaef6-140">System.Boolean</span></span>

## <span data-ttu-id="eaef6-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="eaef6-141">NOTES</span></span>

## <span data-ttu-id="eaef6-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eaef6-142">RELATED LINKS</span></span>
