---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: da4df1206035e5ecae1a21d70e67091e852b1c51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602836"
---
# <span data-ttu-id="389aa-101">Set-AzureRmServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="389aa-101">Set-AzureRmServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="389aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="389aa-102">SYNOPSIS</span></span>
<span data-ttu-id="389aa-103">Esta operação desabilita a recuperação de desastres e interrompe a replicação de alterações de namespaces primário para secundário</span><span class="sxs-lookup"><span data-stu-id="389aa-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="389aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="389aa-104">SYNTAX</span></span>

### <span data-ttu-id="389aa-105">GeoDRBreakPairFailOverPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="389aa-105">GeoDRBreakPairFailOverPropertiesSet (Default)</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="389aa-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="389aa-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="389aa-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="389aa-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="389aa-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="389aa-108">DESCRIPTION</span></span>
<span data-ttu-id="389aa-109">O cmdlet **set-AzureRmServiceBusGeoDRConfigurationBreakPair** desabilita a recuperação de desastres e interrompe a replicação de alterações de namespaces primário para secundário</span><span class="sxs-lookup"><span data-stu-id="389aa-109">The **Set-AzureRmServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="389aa-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="389aa-110">EXAMPLES</span></span>

### <span data-ttu-id="389aa-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="389aa-111">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"
```

<span data-ttu-id="389aa-112">Esta operação desabilita a recuperação de desastres e interrompe a replicação de alterações de namespaces primário para secundário</span><span class="sxs-lookup"><span data-stu-id="389aa-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="389aa-113">OS</span><span class="sxs-lookup"><span data-stu-id="389aa-113">PARAMETERS</span></span>

### <span data-ttu-id="389aa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="389aa-114">-DefaultProfile</span></span>
<span data-ttu-id="389aa-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="389aa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="389aa-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="389aa-116">-InputObject</span></span>
<span data-ttu-id="389aa-117">Objeto de configuração do barramento do serviço GeoDR</span><span class="sxs-lookup"><span data-stu-id="389aa-117">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="389aa-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="389aa-118">-Name</span></span>
<span data-ttu-id="389aa-119">Nome de configuração DR</span><span class="sxs-lookup"><span data-stu-id="389aa-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="389aa-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="389aa-120">-Namespace</span></span>
<span data-ttu-id="389aa-121">Nome do namespace-namespace primário</span><span class="sxs-lookup"><span data-stu-id="389aa-121">Namespace Name - Primary Namespace</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="389aa-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="389aa-122">-PassThru</span></span>
<span data-ttu-id="389aa-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="389aa-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="389aa-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="389aa-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="389aa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="389aa-125">-ResourceGroupName</span></span>
<span data-ttu-id="389aa-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="389aa-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="389aa-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="389aa-127">-ResourceId</span></span>
<span data-ttu-id="389aa-128">ID do recurso GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="389aa-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="389aa-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="389aa-129">-Confirm</span></span>
<span data-ttu-id="389aa-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="389aa-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="389aa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="389aa-131">-WhatIf</span></span>
<span data-ttu-id="389aa-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="389aa-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="389aa-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="389aa-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="389aa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="389aa-134">CommonParameters</span></span>
<span data-ttu-id="389aa-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="389aa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="389aa-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="389aa-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="389aa-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="389aa-137">INPUTS</span></span>

### <span data-ttu-id="389aa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="389aa-138">System.String</span></span>
<span data-ttu-id="389aa-139">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="389aa-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>


## <span data-ttu-id="389aa-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="389aa-140">OUTPUTS</span></span>

### <span data-ttu-id="389aa-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="389aa-141">System.Boolean</span></span>


## <span data-ttu-id="389aa-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="389aa-142">NOTES</span></span>

## <span data-ttu-id="389aa-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="389aa-143">RELATED LINKS</span></span>
