---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: fdd51d73b121feddaf20bbbe48184cc7f565d458
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597897"
---
# <span data-ttu-id="09e25-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="09e25-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="09e25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09e25-102">SYNOPSIS</span></span>
<span data-ttu-id="09e25-103">Remover uma chave de API do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="09e25-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="09e25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09e25-104">SYNTAX</span></span>

### <span data-ttu-id="09e25-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="09e25-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09e25-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09e25-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="09e25-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09e25-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09e25-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="09e25-108">DESCRIPTION</span></span>
<span data-ttu-id="09e25-109">Remover uma chave de API do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="09e25-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="09e25-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09e25-110">EXAMPLES</span></span>

### <span data-ttu-id="09e25-111">Exemplo 1 remover uma chave de API do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="09e25-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Remove-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="09e25-112">Remova a chave de API específica do Application insights que ID é "dd173f38-4fd1-4C75-8af5-9 9c29aa0f867" para o recurso "teste" no grupo de recursos "Test Group".</span><span class="sxs-lookup"><span data-stu-id="09e25-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="09e25-113">OS</span><span class="sxs-lookup"><span data-stu-id="09e25-113">PARAMETERS</span></span>

### <span data-ttu-id="09e25-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="09e25-114">-ApiKeyId</span></span>
<span data-ttu-id="09e25-115">ID da chave de API do Application insights.</span><span class="sxs-lookup"><span data-stu-id="09e25-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="09e25-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="09e25-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="09e25-117">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="09e25-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="09e25-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09e25-118">-DefaultProfile</span></span>
<span data-ttu-id="09e25-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09e25-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09e25-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="09e25-120">-Name</span></span>
<span data-ttu-id="09e25-121">Nome do componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="09e25-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="09e25-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09e25-122">-PassThru</span></span>
<span data-ttu-id="09e25-123">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="09e25-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="09e25-124">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="09e25-124">This parameter is optional.</span></span> <span data-ttu-id="09e25-125">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="09e25-125">Default value is false.</span></span>

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

### <span data-ttu-id="09e25-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09e25-126">-ResourceGroupName</span></span>
<span data-ttu-id="09e25-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="09e25-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="09e25-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09e25-128">-ResourceId</span></span>
<span data-ttu-id="09e25-129">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="09e25-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="09e25-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="09e25-130">-Confirm</span></span>
<span data-ttu-id="09e25-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09e25-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09e25-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09e25-132">-WhatIf</span></span>
<span data-ttu-id="09e25-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="09e25-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09e25-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="09e25-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09e25-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09e25-135">CommonParameters</span></span>
<span data-ttu-id="09e25-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09e25-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09e25-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09e25-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09e25-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="09e25-138">INPUTS</span></span>

### <span data-ttu-id="09e25-139">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="09e25-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="09e25-140">System. String</span><span class="sxs-lookup"><span data-stu-id="09e25-140">System.String</span></span>

## <span data-ttu-id="09e25-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="09e25-141">OUTPUTS</span></span>

### <span data-ttu-id="09e25-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="09e25-142">System.Boolean</span></span>

## <span data-ttu-id="09e25-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="09e25-143">NOTES</span></span>

## <span data-ttu-id="09e25-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09e25-144">RELATED LINKS</span></span>
