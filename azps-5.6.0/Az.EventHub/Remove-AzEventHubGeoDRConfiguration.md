---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 2de5501c63ebbdd8842acb6cbfa40ec51893cbf4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890622"
---
# <span data-ttu-id="521e2-101">Remove-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="521e2-101">Remove-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="521e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="521e2-102">SYNOPSIS</span></span>
<span data-ttu-id="521e2-103">Exclui um Alias(Configuração de Recuperação de Desastre)</span><span class="sxs-lookup"><span data-stu-id="521e2-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="521e2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="521e2-104">SYNTAX</span></span>

### <span data-ttu-id="521e2-105">GeoDRParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="521e2-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="521e2-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="521e2-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="521e2-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="521e2-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="521e2-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="521e2-108">DESCRIPTION</span></span>
<span data-ttu-id="521e2-109">O cmdlet **Remove-AzEventHubGeoDRConfiguration** exclui um Alias(Configuração de Recuperação de Desastre)</span><span class="sxs-lookup"><span data-stu-id="521e2-109">The **Remove-AzEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="521e2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="521e2-110">EXAMPLES</span></span>

### <span data-ttu-id="521e2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="521e2-111">Example 1</span></span>
```
PS C:\>Remove-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="521e2-112">Exclui um Alias (configuração de Recuperação de Desastre)</span><span class="sxs-lookup"><span data-stu-id="521e2-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="521e2-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="521e2-113">PARAMETERS</span></span>

### <span data-ttu-id="521e2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="521e2-114">-AsJob</span></span>
<span data-ttu-id="521e2-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="521e2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="521e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="521e2-116">-DefaultProfile</span></span>
<span data-ttu-id="521e2-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="521e2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="521e2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="521e2-118">-InputObject</span></span>
<span data-ttu-id="521e2-119">Objeto de configuração geográfica eventhub</span><span class="sxs-lookup"><span data-stu-id="521e2-119">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="521e2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="521e2-120">-Name</span></span>
<span data-ttu-id="521e2-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="521e2-121">Alias (GeoDR)</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="521e2-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="521e2-122">-Namespace</span></span>
<span data-ttu-id="521e2-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="521e2-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="521e2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="521e2-124">-PassThru</span></span>
<span data-ttu-id="521e2-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="521e2-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="521e2-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="521e2-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="521e2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="521e2-127">-ResourceGroupName</span></span>
<span data-ttu-id="521e2-128">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="521e2-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="521e2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="521e2-129">-ResourceId</span></span>
<span data-ttu-id="521e2-130">ID do Recurso GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="521e2-130">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="521e2-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="521e2-131">-Confirm</span></span>
<span data-ttu-id="521e2-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="521e2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="521e2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="521e2-133">-WhatIf</span></span>
<span data-ttu-id="521e2-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="521e2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="521e2-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="521e2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="521e2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="521e2-136">CommonParameters</span></span>
<span data-ttu-id="521e2-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="521e2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="521e2-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="521e2-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="521e2-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="521e2-139">INPUTS</span></span>

### <span data-ttu-id="521e2-140">System.String</span><span class="sxs-lookup"><span data-stu-id="521e2-140">System.String</span></span>

### <span data-ttu-id="521e2-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="521e2-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="521e2-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="521e2-142">OUTPUTS</span></span>

### <span data-ttu-id="521e2-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="521e2-143">System.Boolean</span></span>

## <span data-ttu-id="521e2-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="521e2-144">NOTES</span></span>

## <span data-ttu-id="521e2-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="521e2-145">RELATED LINKS</span></span>
