---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: b63f1b350daad55a26dc91f46e89b28675622fbb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112280"
---
# <span data-ttu-id="531dc-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="531dc-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="531dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="531dc-102">SYNOPSIS</span></span>
<span data-ttu-id="531dc-103">Remover um recurso de informações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="531dc-103">Remove an application insights resource</span></span>

## <span data-ttu-id="531dc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="531dc-104">SYNTAX</span></span>

### <span data-ttu-id="531dc-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="531dc-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="531dc-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="531dc-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="531dc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="531dc-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="531dc-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="531dc-108">DESCRIPTION</span></span>
<span data-ttu-id="531dc-109">Remover um recurso de informações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="531dc-109">Remove an application insights resource</span></span>

## <span data-ttu-id="531dc-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="531dc-110">EXAMPLES</span></span>

### <span data-ttu-id="531dc-111">Exemplo 1 Remover um recurso de ideias de aplicativo</span><span class="sxs-lookup"><span data-stu-id="531dc-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="531dc-112">Remover um recurso de ideias de aplicativo chamado "teste" no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="531dc-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="531dc-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="531dc-113">PARAMETERS</span></span>

### <span data-ttu-id="531dc-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="531dc-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="531dc-115">Objeto componente Do Insights do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="531dc-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="531dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="531dc-116">-DefaultProfile</span></span>
<span data-ttu-id="531dc-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="531dc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="531dc-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="531dc-118">-Name</span></span>
<span data-ttu-id="531dc-119">Nome do componente Informações do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="531dc-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="531dc-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="531dc-120">-PassThru</span></span>
<span data-ttu-id="531dc-121">Se especificado, a gravação será verdadeira caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="531dc-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="531dc-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="531dc-122">This parameter is optional.</span></span> <span data-ttu-id="531dc-123">O valor padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="531dc-123">Default value is false.</span></span>

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

### <span data-ttu-id="531dc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="531dc-124">-ResourceGroupName</span></span>
<span data-ttu-id="531dc-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="531dc-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="531dc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="531dc-126">-ResourceId</span></span>
<span data-ttu-id="531dc-127">ID do Recurso de Componentes do Insights do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="531dc-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="531dc-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="531dc-128">-Confirm</span></span>
<span data-ttu-id="531dc-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="531dc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="531dc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="531dc-130">-WhatIf</span></span>
<span data-ttu-id="531dc-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="531dc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="531dc-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="531dc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="531dc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="531dc-133">CommonParameters</span></span>
<span data-ttu-id="531dc-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="531dc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="531dc-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="531dc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="531dc-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="531dc-136">INPUTS</span></span>

### <span data-ttu-id="531dc-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="531dc-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="531dc-138">System.String</span><span class="sxs-lookup"><span data-stu-id="531dc-138">System.String</span></span>

## <span data-ttu-id="531dc-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="531dc-139">OUTPUTS</span></span>

### <span data-ttu-id="531dc-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="531dc-140">System.Boolean</span></span>

## <span data-ttu-id="531dc-141">Notas</span><span class="sxs-lookup"><span data-stu-id="531dc-141">NOTES</span></span>

## <span data-ttu-id="531dc-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="531dc-142">RELATED LINKS</span></span>
