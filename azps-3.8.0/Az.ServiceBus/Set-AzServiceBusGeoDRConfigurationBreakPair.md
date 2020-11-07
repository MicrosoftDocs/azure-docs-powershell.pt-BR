---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: f45899b1c2d397245461a10a6e2648f92dc9da40
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941094"
---
# <span data-ttu-id="bef5c-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="bef5c-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="bef5c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bef5c-102">SYNOPSIS</span></span>
<span data-ttu-id="bef5c-103">Esta operação desabilita a recuperação de desastres e interrompe a replicação de alterações de namespaces primário para secundário</span><span class="sxs-lookup"><span data-stu-id="bef5c-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="bef5c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bef5c-104">SYNTAX</span></span>

### <span data-ttu-id="bef5c-105">GeoDRPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="bef5c-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bef5c-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bef5c-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bef5c-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bef5c-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bef5c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bef5c-108">DESCRIPTION</span></span>
<span data-ttu-id="bef5c-109">O cmdlet **set-AzServiceBusGeoDRConfigurationBreakPair** desabilita a recuperação de desastres e interrompe a replicação de alterações de namespaces primário para secundário</span><span class="sxs-lookup"><span data-stu-id="bef5c-109">The **Set-AzServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="bef5c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bef5c-110">EXAMPLES</span></span>

### <span data-ttu-id="bef5c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bef5c-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="bef5c-112">Esta operação desabilita a recuperação de desastres e interrompe a replicação de alterações de namespaces primário para secundário</span><span class="sxs-lookup"><span data-stu-id="bef5c-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="bef5c-113">OS</span><span class="sxs-lookup"><span data-stu-id="bef5c-113">PARAMETERS</span></span>

### <span data-ttu-id="bef5c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bef5c-114">-DefaultProfile</span></span>
<span data-ttu-id="bef5c-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bef5c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bef5c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bef5c-116">-InputObject</span></span>
<span data-ttu-id="bef5c-117">Objeto de configuração do barramento do serviço GeoDR</span><span class="sxs-lookup"><span data-stu-id="bef5c-117">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bef5c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="bef5c-118">-Name</span></span>
<span data-ttu-id="bef5c-119">Nome de configuração DR</span><span class="sxs-lookup"><span data-stu-id="bef5c-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef5c-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bef5c-120">-Namespace</span></span>
<span data-ttu-id="bef5c-121">Nome do namespace-namespace primário</span><span class="sxs-lookup"><span data-stu-id="bef5c-121">Namespace Name - Primary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef5c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bef5c-122">-PassThru</span></span>
<span data-ttu-id="bef5c-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="bef5c-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bef5c-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="bef5c-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bef5c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bef5c-125">-ResourceGroupName</span></span>
<span data-ttu-id="bef5c-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="bef5c-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef5c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bef5c-127">-ResourceId</span></span>
<span data-ttu-id="bef5c-128">ID do recurso GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="bef5c-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="bef5c-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bef5c-129">-Confirm</span></span>
<span data-ttu-id="bef5c-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bef5c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bef5c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bef5c-131">-WhatIf</span></span>
<span data-ttu-id="bef5c-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bef5c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bef5c-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bef5c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bef5c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bef5c-134">CommonParameters</span></span>
<span data-ttu-id="bef5c-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bef5c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bef5c-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bef5c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bef5c-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bef5c-137">INPUTS</span></span>

### <span data-ttu-id="bef5c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="bef5c-138">System.String</span></span>

### <span data-ttu-id="bef5c-139">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="bef5c-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="bef5c-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bef5c-140">OUTPUTS</span></span>

### <span data-ttu-id="bef5c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bef5c-141">System.Boolean</span></span>

## <span data-ttu-id="bef5c-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bef5c-142">NOTES</span></span>

## <span data-ttu-id="bef5c-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bef5c-143">RELATED LINKS</span></span>
