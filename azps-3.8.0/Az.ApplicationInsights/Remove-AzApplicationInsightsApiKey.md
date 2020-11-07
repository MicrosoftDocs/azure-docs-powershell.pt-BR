---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 53ebb6d1a7bcfc35dafb09c377b2a4a023e327d8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942808"
---
# <span data-ttu-id="42187-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="42187-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="42187-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="42187-102">SYNOPSIS</span></span>
<span data-ttu-id="42187-103">Remover uma chave de API do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="42187-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="42187-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42187-104">SYNTAX</span></span>

### <span data-ttu-id="42187-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="42187-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42187-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42187-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42187-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42187-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42187-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="42187-108">DESCRIPTION</span></span>
<span data-ttu-id="42187-109">Remover uma chave de API do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="42187-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="42187-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42187-110">EXAMPLES</span></span>

### <span data-ttu-id="42187-111">Exemplo 1 remover uma chave de API do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="42187-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Remove-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="42187-112">Remova a chave de API específica do Application insights que ID é "dd173f38-4fd1-4C75-8af5-9 9c29aa0f867" para o recurso "teste" no grupo de recursos "Test Group".</span><span class="sxs-lookup"><span data-stu-id="42187-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="42187-113">OS</span><span class="sxs-lookup"><span data-stu-id="42187-113">PARAMETERS</span></span>

### <span data-ttu-id="42187-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="42187-114">-ApiKeyId</span></span>
<span data-ttu-id="42187-115">ID da chave de API do Application insights.</span><span class="sxs-lookup"><span data-stu-id="42187-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="42187-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="42187-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="42187-117">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="42187-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="42187-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42187-118">-DefaultProfile</span></span>
<span data-ttu-id="42187-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="42187-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42187-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="42187-120">-Name</span></span>
<span data-ttu-id="42187-121">Nome do componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="42187-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="42187-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42187-122">-PassThru</span></span>
<span data-ttu-id="42187-123">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="42187-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="42187-124">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="42187-124">This parameter is optional.</span></span> <span data-ttu-id="42187-125">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="42187-125">Default value is false.</span></span>

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

### <span data-ttu-id="42187-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42187-126">-ResourceGroupName</span></span>
<span data-ttu-id="42187-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="42187-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="42187-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42187-128">-ResourceId</span></span>
<span data-ttu-id="42187-129">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="42187-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="42187-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="42187-130">-Confirm</span></span>
<span data-ttu-id="42187-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42187-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42187-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42187-132">-WhatIf</span></span>
<span data-ttu-id="42187-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="42187-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42187-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="42187-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42187-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42187-135">CommonParameters</span></span>
<span data-ttu-id="42187-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42187-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42187-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42187-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42187-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="42187-138">INPUTS</span></span>

### <span data-ttu-id="42187-139">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="42187-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="42187-140">System. String</span><span class="sxs-lookup"><span data-stu-id="42187-140">System.String</span></span>

## <span data-ttu-id="42187-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="42187-141">OUTPUTS</span></span>

### <span data-ttu-id="42187-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="42187-142">System.Boolean</span></span>

## <span data-ttu-id="42187-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="42187-143">NOTES</span></span>

## <span data-ttu-id="42187-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42187-144">RELATED LINKS</span></span>
