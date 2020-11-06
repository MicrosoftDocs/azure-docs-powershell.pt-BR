---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: a12f22260ce8ee5412cd17ddfa420a7d23f82008
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430025"
---
# <span data-ttu-id="0bb3e-101">Set-AzureRmServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="0bb3e-101">Set-AzureRmServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="0bb3e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0bb3e-102">SYNOPSIS</span></span>
<span data-ttu-id="0bb3e-103">Esta operação desabilita a recuperação de desastres e interrompe a replicação de alterações de namespaces primário para secundário</span><span class="sxs-lookup"><span data-stu-id="0bb3e-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bb3e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0bb3e-104">SYNTAX</span></span>

### <span data-ttu-id="0bb3e-105">GeoDRPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0bb3e-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0bb3e-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0bb3e-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bb3e-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bb3e-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bb3e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0bb3e-108">DESCRIPTION</span></span>
<span data-ttu-id="0bb3e-109">O cmdlet **set-AzureRmServiceBusGeoDRConfigurationBreakPair** desabilita a recuperação de desastres e interrompe a replicação de alterações de namespaces primário para secundário</span><span class="sxs-lookup"><span data-stu-id="0bb3e-109">The **Set-AzureRmServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="0bb3e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0bb3e-110">EXAMPLES</span></span>

### <span data-ttu-id="0bb3e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0bb3e-111">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"
```

<span data-ttu-id="0bb3e-112">Esta operação desabilita a recuperação de desastres e interrompe a replicação de alterações de namespaces primário para secundário</span><span class="sxs-lookup"><span data-stu-id="0bb3e-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="0bb3e-113">OS</span><span class="sxs-lookup"><span data-stu-id="0bb3e-113">PARAMETERS</span></span>

### <span data-ttu-id="0bb3e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bb3e-114">-DefaultProfile</span></span>
<span data-ttu-id="0bb3e-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0bb3e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb3e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0bb3e-116">-InputObject</span></span>
<span data-ttu-id="0bb3e-117">Objeto de configuração do barramento do serviço GeoDR</span><span class="sxs-lookup"><span data-stu-id="0bb3e-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="0bb3e-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="0bb3e-118">-Name</span></span>
<span data-ttu-id="0bb3e-119">Nome de configuração DR</span><span class="sxs-lookup"><span data-stu-id="0bb3e-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="0bb3e-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0bb3e-120">-Namespace</span></span>
<span data-ttu-id="0bb3e-121">Nome do namespace-namespace primário</span><span class="sxs-lookup"><span data-stu-id="0bb3e-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="0bb3e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bb3e-122">-PassThru</span></span>
<span data-ttu-id="0bb3e-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="0bb3e-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0bb3e-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="0bb3e-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0bb3e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bb3e-125">-ResourceGroupName</span></span>
<span data-ttu-id="0bb3e-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0bb3e-126">Resource Group Name</span></span>

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

### <span data-ttu-id="0bb3e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bb3e-127">-ResourceId</span></span>
<span data-ttu-id="0bb3e-128">ID do recurso GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="0bb3e-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="0bb3e-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0bb3e-129">-Confirm</span></span>
<span data-ttu-id="0bb3e-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bb3e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bb3e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bb3e-131">-WhatIf</span></span>
<span data-ttu-id="0bb3e-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0bb3e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bb3e-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0bb3e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bb3e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bb3e-134">CommonParameters</span></span>
<span data-ttu-id="0bb3e-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bb3e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bb3e-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bb3e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bb3e-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0bb3e-137">INPUTS</span></span>

### <span data-ttu-id="0bb3e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0bb3e-138">System.String</span></span>

### <span data-ttu-id="0bb3e-139">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="0bb3e-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="0bb3e-140">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0bb3e-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="0bb3e-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0bb3e-141">OUTPUTS</span></span>

### <span data-ttu-id="0bb3e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0bb3e-142">System.Boolean</span></span>

## <span data-ttu-id="0bb3e-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0bb3e-143">NOTES</span></span>

## <span data-ttu-id="0bb3e-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0bb3e-144">RELATED LINKS</span></span>
