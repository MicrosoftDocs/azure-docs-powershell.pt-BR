---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: d68fe2005f827d55b57ecedb7e21fd11b0cc9978
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889672"
---
# <span data-ttu-id="17187-101">Set-AzEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="17187-101">Set-AzEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="17187-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17187-102">SYNOPSIS</span></span>
<span data-ttu-id="17187-103">Invoca o failover de DR GEO e reconfigura o alias para apontar para o namespace secundário</span><span class="sxs-lookup"><span data-stu-id="17187-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="17187-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="17187-104">SYNTAX</span></span>

### <span data-ttu-id="17187-105">GeoDRParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="17187-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17187-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="17187-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17187-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="17187-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17187-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="17187-108">DESCRIPTION</span></span>
<span data-ttu-id="17187-109">O cmdlet **Set-AzEventHubGeoDRConfigurationFailOver** invoca o failover de DR GEO e reconfigura o alias para apontar para o namespace secundário</span><span class="sxs-lookup"><span data-stu-id="17187-109">The **Set-AzEventHubGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="17187-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17187-110">EXAMPLES</span></span>

### <span data-ttu-id="17187-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="17187-111">Example 1</span></span>
```
PS C:\>Set-AzEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="17187-112">Invoca o Failover sobre o alias "SampleDRConfigName", reconfigura e aponta para namespace secundário "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="17187-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="17187-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="17187-113">PARAMETERS</span></span>

### <span data-ttu-id="17187-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17187-114">-DefaultProfile</span></span>
<span data-ttu-id="17187-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17187-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17187-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17187-116">-InputObject</span></span>
<span data-ttu-id="17187-117">Objeto de configuração geográfica eventhub</span><span class="sxs-lookup"><span data-stu-id="17187-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="17187-118">-Name</span><span class="sxs-lookup"><span data-stu-id="17187-118">-Name</span></span>
<span data-ttu-id="17187-119">Nome da configuração dr</span><span class="sxs-lookup"><span data-stu-id="17187-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="17187-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="17187-120">-Namespace</span></span>
<span data-ttu-id="17187-121">Namespace Name - Namespace secundário</span><span class="sxs-lookup"><span data-stu-id="17187-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="17187-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17187-122">-PassThru</span></span>
<span data-ttu-id="17187-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="17187-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="17187-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="17187-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="17187-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17187-125">-ResourceGroupName</span></span>
<span data-ttu-id="17187-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="17187-126">Resource Group Name</span></span>

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

### <span data-ttu-id="17187-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17187-127">-ResourceId</span></span>
<span data-ttu-id="17187-128">ID do Recurso GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="17187-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="17187-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17187-129">-Confirm</span></span>
<span data-ttu-id="17187-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17187-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17187-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17187-131">-WhatIf</span></span>
<span data-ttu-id="17187-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="17187-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17187-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="17187-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17187-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17187-134">CommonParameters</span></span>
<span data-ttu-id="17187-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17187-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17187-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17187-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17187-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17187-137">INPUTS</span></span>

### <span data-ttu-id="17187-138">System.String</span><span class="sxs-lookup"><span data-stu-id="17187-138">System.String</span></span>

### <span data-ttu-id="17187-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="17187-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="17187-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="17187-140">OUTPUTS</span></span>

### <span data-ttu-id="17187-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="17187-141">System.Boolean</span></span>

## <span data-ttu-id="17187-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="17187-142">NOTES</span></span>

## <span data-ttu-id="17187-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17187-143">RELATED LINKS</span></span>
