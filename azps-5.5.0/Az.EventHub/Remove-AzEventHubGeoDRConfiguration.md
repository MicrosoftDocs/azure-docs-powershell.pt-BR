---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 57a4ee870e10b04e4c5e58e34122376a790ce6d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117658"
---
# <span data-ttu-id="88242-101">Remove-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="88242-101">Remove-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="88242-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88242-102">SYNOPSIS</span></span>
<span data-ttu-id="88242-103">Exclui um Alias(Configuração de Recuperação de Desastres)</span><span class="sxs-lookup"><span data-stu-id="88242-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="88242-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88242-104">SYNTAX</span></span>

### <span data-ttu-id="88242-105">GeoDRParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="88242-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88242-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="88242-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88242-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88242-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88242-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="88242-108">DESCRIPTION</span></span>
<span data-ttu-id="88242-109">O cmdlet **Remove-AzEventHubGeoDRConfiguration** exclui um Alias(configuração de Recuperação de Desastres)</span><span class="sxs-lookup"><span data-stu-id="88242-109">The **Remove-AzEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="88242-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="88242-110">EXAMPLES</span></span>

### <span data-ttu-id="88242-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="88242-111">Example 1</span></span>
```
PS C:\>Remove-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="88242-112">Exclui um Alias (configuração de Recuperação de Desastres)</span><span class="sxs-lookup"><span data-stu-id="88242-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="88242-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88242-113">PARAMETERS</span></span>

### <span data-ttu-id="88242-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88242-114">-AsJob</span></span>
<span data-ttu-id="88242-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="88242-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88242-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88242-116">-DefaultProfile</span></span>
<span data-ttu-id="88242-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="88242-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88242-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88242-118">-InputObject</span></span>
<span data-ttu-id="88242-119">Objeto de configuração geodr do Eventhub</span><span class="sxs-lookup"><span data-stu-id="88242-119">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="88242-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="88242-120">-Name</span></span>
<span data-ttu-id="88242-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="88242-121">Alias (GeoDR)</span></span>

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

### <span data-ttu-id="88242-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="88242-122">-Namespace</span></span>
<span data-ttu-id="88242-123">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="88242-123">Namespace Name</span></span>

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

### <span data-ttu-id="88242-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88242-124">-PassThru</span></span>
<span data-ttu-id="88242-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="88242-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="88242-126">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="88242-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="88242-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88242-127">-ResourceGroupName</span></span>
<span data-ttu-id="88242-128">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="88242-128">Resource Group Name</span></span>

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

### <span data-ttu-id="88242-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88242-129">-ResourceId</span></span>
<span data-ttu-id="88242-130">ID do Recurso GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="88242-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="88242-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="88242-131">-Confirm</span></span>
<span data-ttu-id="88242-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88242-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88242-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88242-133">-WhatIf</span></span>
<span data-ttu-id="88242-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="88242-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88242-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="88242-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88242-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88242-136">CommonParameters</span></span>
<span data-ttu-id="88242-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88242-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88242-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88242-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88242-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="88242-139">INPUTS</span></span>

### <span data-ttu-id="88242-140">System.String</span><span class="sxs-lookup"><span data-stu-id="88242-140">System.String</span></span>

### <span data-ttu-id="88242-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="88242-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="88242-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="88242-142">OUTPUTS</span></span>

### <span data-ttu-id="88242-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="88242-143">System.Boolean</span></span>

## <span data-ttu-id="88242-144">Notas</span><span class="sxs-lookup"><span data-stu-id="88242-144">NOTES</span></span>

## <span data-ttu-id="88242-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88242-145">RELATED LINKS</span></span>
