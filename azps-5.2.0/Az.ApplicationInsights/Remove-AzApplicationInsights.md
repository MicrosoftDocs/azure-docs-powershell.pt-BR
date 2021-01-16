---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: b63f1b350daad55a26dc91f46e89b28675622fbb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261625"
---
# <span data-ttu-id="df1f6-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="df1f6-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="df1f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df1f6-102">SYNOPSIS</span></span>
<span data-ttu-id="df1f6-103">Remover um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="df1f6-103">Remove an application insights resource</span></span>

## <span data-ttu-id="df1f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df1f6-104">SYNTAX</span></span>

### <span data-ttu-id="df1f6-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="df1f6-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df1f6-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df1f6-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df1f6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="df1f6-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df1f6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df1f6-108">DESCRIPTION</span></span>
<span data-ttu-id="df1f6-109">Remover um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="df1f6-109">Remove an application insights resource</span></span>

## <span data-ttu-id="df1f6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df1f6-110">EXAMPLES</span></span>

### <span data-ttu-id="df1f6-111">Exemplo 1 remover um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="df1f6-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="df1f6-112">Remover um recurso do Application insights chamado "Test" no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="df1f6-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="df1f6-113">OS</span><span class="sxs-lookup"><span data-stu-id="df1f6-113">PARAMETERS</span></span>

### <span data-ttu-id="df1f6-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="df1f6-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="df1f6-115">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="df1f6-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="df1f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df1f6-116">-DefaultProfile</span></span>
<span data-ttu-id="df1f6-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df1f6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df1f6-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="df1f6-118">-Name</span></span>
<span data-ttu-id="df1f6-119">Nome do componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="df1f6-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="df1f6-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df1f6-120">-PassThru</span></span>
<span data-ttu-id="df1f6-121">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="df1f6-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="df1f6-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="df1f6-122">This parameter is optional.</span></span> <span data-ttu-id="df1f6-123">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="df1f6-123">Default value is false.</span></span>

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

### <span data-ttu-id="df1f6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df1f6-124">-ResourceGroupName</span></span>
<span data-ttu-id="df1f6-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="df1f6-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="df1f6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df1f6-126">-ResourceId</span></span>
<span data-ttu-id="df1f6-127">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="df1f6-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="df1f6-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="df1f6-128">-Confirm</span></span>
<span data-ttu-id="df1f6-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df1f6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df1f6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df1f6-130">-WhatIf</span></span>
<span data-ttu-id="df1f6-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="df1f6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df1f6-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="df1f6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df1f6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df1f6-133">CommonParameters</span></span>
<span data-ttu-id="df1f6-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df1f6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df1f6-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df1f6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df1f6-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df1f6-136">INPUTS</span></span>

### <span data-ttu-id="df1f6-137">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="df1f6-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="df1f6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="df1f6-138">System.String</span></span>

## <span data-ttu-id="df1f6-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df1f6-139">OUTPUTS</span></span>

### <span data-ttu-id="df1f6-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="df1f6-140">System.Boolean</span></span>

## <span data-ttu-id="df1f6-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df1f6-141">NOTES</span></span>

## <span data-ttu-id="df1f6-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df1f6-142">RELATED LINKS</span></span>
