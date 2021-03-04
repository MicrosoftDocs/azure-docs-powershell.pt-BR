---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 95f99f629fd32333e06c6194fcaf51837224f4a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885897"
---
# <span data-ttu-id="8bbb6-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="8bbb6-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="8bbb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bbb6-102">SYNOPSIS</span></span>
<span data-ttu-id="8bbb6-103">Remover uma chave de api de insights de aplicativo para um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="8bbb6-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="8bbb6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8bbb6-104">SYNTAX</span></span>

### <span data-ttu-id="8bbb6-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8bbb6-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bbb6-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bbb6-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8bbb6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bbb6-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bbb6-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8bbb6-108">DESCRIPTION</span></span>
<span data-ttu-id="8bbb6-109">Remover uma chave de api de insights de aplicativo para um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="8bbb6-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="8bbb6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8bbb6-110">EXAMPLES</span></span>

### <span data-ttu-id="8bbb6-111">Exemplo 1 Remover uma chave de api de insights de aplicativo para um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="8bbb6-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Remove-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="8bbb6-112">Remova a chave de api de percepções de aplicativo específica que id é "dd173f38-4fd1-4c75-8af5-9 9c29aaa0f867" para o recurso "test" no grupo de recursos "testGroup".</span><span class="sxs-lookup"><span data-stu-id="8bbb6-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="8bbb6-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8bbb6-113">PARAMETERS</span></span>

### <span data-ttu-id="8bbb6-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="8bbb6-114">-ApiKeyId</span></span>
<span data-ttu-id="8bbb6-115">ID da chave da API do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8bbb6-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="8bbb6-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8bbb6-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="8bbb6-117">Objeto Application Insights Component.</span><span class="sxs-lookup"><span data-stu-id="8bbb6-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="8bbb6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bbb6-118">-DefaultProfile</span></span>
<span data-ttu-id="8bbb6-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8bbb6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bbb6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8bbb6-120">-Name</span></span>
<span data-ttu-id="8bbb6-121">Nome do componente do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8bbb6-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="8bbb6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8bbb6-122">-PassThru</span></span>
<span data-ttu-id="8bbb6-123">Se especificado, a gravação será true caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8bbb6-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="8bbb6-124">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="8bbb6-124">This parameter is optional.</span></span> <span data-ttu-id="8bbb6-125">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="8bbb6-125">Default value is false.</span></span>

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

### <span data-ttu-id="8bbb6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bbb6-126">-ResourceGroupName</span></span>
<span data-ttu-id="8bbb6-127">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="8bbb6-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="8bbb6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bbb6-128">-ResourceId</span></span>
<span data-ttu-id="8bbb6-129">ID do Recurso de Componente do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8bbb6-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="8bbb6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8bbb6-130">-Confirm</span></span>
<span data-ttu-id="8bbb6-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bbb6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bbb6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bbb6-132">-WhatIf</span></span>
<span data-ttu-id="8bbb6-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8bbb6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bbb6-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8bbb6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bbb6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bbb6-135">CommonParameters</span></span>
<span data-ttu-id="8bbb6-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bbb6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bbb6-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bbb6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bbb6-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8bbb6-138">INPUTS</span></span>

### <span data-ttu-id="8bbb6-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8bbb6-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="8bbb6-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8bbb6-140">System.String</span></span>

## <span data-ttu-id="8bbb6-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8bbb6-141">OUTPUTS</span></span>

### <span data-ttu-id="8bbb6-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8bbb6-142">System.Boolean</span></span>

## <span data-ttu-id="8bbb6-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="8bbb6-143">NOTES</span></span>

## <span data-ttu-id="8bbb6-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8bbb6-144">RELATED LINKS</span></span>
