---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 57a4ee870e10b04e4c5e58e34122376a790ce6d4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777529"
---
# <span data-ttu-id="d0fd3-101">Remove-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0fd3-101">Remove-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="d0fd3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0fd3-102">SYNOPSIS</span></span>
<span data-ttu-id="d0fd3-103">Exclui um alias (configuração de recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="d0fd3-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="d0fd3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0fd3-104">SYNTAX</span></span>

### <span data-ttu-id="d0fd3-105">GeoDRParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d0fd3-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0fd3-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d0fd3-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0fd3-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0fd3-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0fd3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d0fd3-108">DESCRIPTION</span></span>
<span data-ttu-id="d0fd3-109">O cmdlet **Remove-AzEventHubGeoDRConfiguration** exclui um alias (configuração de recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="d0fd3-109">The **Remove-AzEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="d0fd3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0fd3-110">EXAMPLES</span></span>

### <span data-ttu-id="d0fd3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d0fd3-111">Example 1</span></span>
```
PS C:\>Remove-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="d0fd3-112">Exclui um alias (configuração de recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="d0fd3-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="d0fd3-113">OS</span><span class="sxs-lookup"><span data-stu-id="d0fd3-113">PARAMETERS</span></span>

### <span data-ttu-id="d0fd3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0fd3-114">-AsJob</span></span>
<span data-ttu-id="d0fd3-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d0fd3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0fd3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0fd3-116">-DefaultProfile</span></span>
<span data-ttu-id="d0fd3-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d0fd3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0fd3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0fd3-118">-InputObject</span></span>
<span data-ttu-id="d0fd3-119">Objeto de configuração GeoDR do Eventhub</span><span class="sxs-lookup"><span data-stu-id="d0fd3-119">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="d0fd3-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d0fd3-120">-Name</span></span>
<span data-ttu-id="d0fd3-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="d0fd3-121">Alias (GeoDR)</span></span>

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

### <span data-ttu-id="d0fd3-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d0fd3-122">-Namespace</span></span>
<span data-ttu-id="d0fd3-123">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="d0fd3-123">Namespace Name</span></span>

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

### <span data-ttu-id="d0fd3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0fd3-124">-PassThru</span></span>
<span data-ttu-id="d0fd3-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="d0fd3-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d0fd3-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="d0fd3-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d0fd3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0fd3-127">-ResourceGroupName</span></span>
<span data-ttu-id="d0fd3-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d0fd3-128">Resource Group Name</span></span>

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

### <span data-ttu-id="d0fd3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0fd3-129">-ResourceId</span></span>
<span data-ttu-id="d0fd3-130">ID do recurso GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0fd3-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="d0fd3-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d0fd3-131">-Confirm</span></span>
<span data-ttu-id="d0fd3-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0fd3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0fd3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0fd3-133">-WhatIf</span></span>
<span data-ttu-id="d0fd3-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d0fd3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0fd3-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d0fd3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0fd3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0fd3-136">CommonParameters</span></span>
<span data-ttu-id="d0fd3-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0fd3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0fd3-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0fd3-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0fd3-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d0fd3-139">INPUTS</span></span>

### <span data-ttu-id="d0fd3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d0fd3-140">System.String</span></span>

### <span data-ttu-id="d0fd3-141">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="d0fd3-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="d0fd3-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d0fd3-142">OUTPUTS</span></span>

### <span data-ttu-id="d0fd3-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d0fd3-143">System.Boolean</span></span>

## <span data-ttu-id="d0fd3-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d0fd3-144">NOTES</span></span>

## <span data-ttu-id="d0fd3-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0fd3-145">RELATED LINKS</span></span>
