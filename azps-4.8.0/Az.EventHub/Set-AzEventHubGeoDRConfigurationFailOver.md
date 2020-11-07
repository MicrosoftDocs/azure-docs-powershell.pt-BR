---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 4ee96fbe20fca3f0af1f0bb9604f178b912d0ea2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948283"
---
# <span data-ttu-id="3f787-101">Set-AzEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="3f787-101">Set-AzEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="3f787-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f787-102">SYNOPSIS</span></span>
<span data-ttu-id="3f787-103">Invoca o failover de DR geográfico e reconfigura o alias para apontar para o namespace secundário</span><span class="sxs-lookup"><span data-stu-id="3f787-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="3f787-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f787-104">SYNTAX</span></span>

### <span data-ttu-id="3f787-105">GeoDRParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3f787-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f787-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3f787-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f787-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f787-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f787-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3f787-108">DESCRIPTION</span></span>
<span data-ttu-id="3f787-109">O cmdlet **set-AzEventHubGeoDRConfigurationFailOver** invoca o failover de Dr geográfico e reconfigura o alias para apontar para o namespace secundário</span><span class="sxs-lookup"><span data-stu-id="3f787-109">The **Set-AzEventHubGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="3f787-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f787-110">EXAMPLES</span></span>

### <span data-ttu-id="3f787-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3f787-111">Example 1</span></span>
```
PS C:\>Set-AzEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="3f787-112">Invoca o failover por alias "SampleDRConfigName", reconfigura e aponta para o namespace secundário "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="3f787-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="3f787-113">OS</span><span class="sxs-lookup"><span data-stu-id="3f787-113">PARAMETERS</span></span>

### <span data-ttu-id="3f787-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f787-114">-DefaultProfile</span></span>
<span data-ttu-id="3f787-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f787-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f787-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f787-116">-InputObject</span></span>
<span data-ttu-id="3f787-117">Objeto de configuração GeoDR do Eventhub</span><span class="sxs-lookup"><span data-stu-id="3f787-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="3f787-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f787-118">-Name</span></span>
<span data-ttu-id="3f787-119">Nome de configuração DR</span><span class="sxs-lookup"><span data-stu-id="3f787-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="3f787-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3f787-120">-Namespace</span></span>
<span data-ttu-id="3f787-121">Nome do namespace-namespace secundário</span><span class="sxs-lookup"><span data-stu-id="3f787-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="3f787-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f787-122">-PassThru</span></span>
<span data-ttu-id="3f787-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="3f787-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3f787-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="3f787-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3f787-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f787-125">-ResourceGroupName</span></span>
<span data-ttu-id="3f787-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3f787-126">Resource Group Name</span></span>

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

### <span data-ttu-id="3f787-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f787-127">-ResourceId</span></span>
<span data-ttu-id="3f787-128">ID do recurso GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f787-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="3f787-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3f787-129">-Confirm</span></span>
<span data-ttu-id="3f787-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f787-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f787-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f787-131">-WhatIf</span></span>
<span data-ttu-id="3f787-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3f787-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f787-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3f787-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f787-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f787-134">CommonParameters</span></span>
<span data-ttu-id="3f787-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f787-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f787-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f787-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f787-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3f787-137">INPUTS</span></span>

### <span data-ttu-id="3f787-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3f787-138">System.String</span></span>

### <span data-ttu-id="3f787-139">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="3f787-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="3f787-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3f787-140">OUTPUTS</span></span>

### <span data-ttu-id="3f787-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3f787-141">System.Boolean</span></span>

## <span data-ttu-id="3f787-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3f787-142">NOTES</span></span>

## <span data-ttu-id="3f787-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f787-143">RELATED LINKS</span></span>
