---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 581f3c24c8c195b1cafc4962d1c6319418cc07f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429336"
---
# <span data-ttu-id="468b3-101">Remove-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="468b3-101">Remove-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="468b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="468b3-102">SYNOPSIS</span></span>
<span data-ttu-id="468b3-103">Exclui um alias (configuração de recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="468b3-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="468b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="468b3-104">SYNTAX</span></span>

### <span data-ttu-id="468b3-105">GeoDRPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="468b3-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="468b3-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="468b3-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="468b3-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="468b3-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="468b3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="468b3-108">DESCRIPTION</span></span>
<span data-ttu-id="468b3-109">O cmdlet **Remove-AzureRmServiceBusGeoDRConfiguration** exclui um alias (configuração de recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="468b3-109">The **Remove-AzureRmServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="468b3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="468b3-110">EXAMPLES</span></span>

### <span data-ttu-id="468b3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="468b3-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="468b3-112">Exclui um alias (configuração de recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="468b3-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="468b3-113">OS</span><span class="sxs-lookup"><span data-stu-id="468b3-113">PARAMETERS</span></span>

### <span data-ttu-id="468b3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="468b3-114">-AsJob</span></span>
<span data-ttu-id="468b3-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="468b3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="468b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="468b3-116">-DefaultProfile</span></span>
<span data-ttu-id="468b3-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="468b3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="468b3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="468b3-118">-InputObject</span></span>
<span data-ttu-id="468b3-119">Objeto de configuração do barramento do serviço GeoDR</span><span class="sxs-lookup"><span data-stu-id="468b3-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="468b3-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="468b3-120">-Name</span></span>
<span data-ttu-id="468b3-121">Nome do alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="468b3-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="468b3-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="468b3-122">-Namespace</span></span>
<span data-ttu-id="468b3-123">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="468b3-123">Namespace Name</span></span>

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

### <span data-ttu-id="468b3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="468b3-124">-PassThru</span></span>
<span data-ttu-id="468b3-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="468b3-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="468b3-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="468b3-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="468b3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="468b3-127">-ResourceGroupName</span></span>
<span data-ttu-id="468b3-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="468b3-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="468b3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="468b3-129">-ResourceId</span></span>
<span data-ttu-id="468b3-130">ID do recurso GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="468b3-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="468b3-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="468b3-131">-Confirm</span></span>
<span data-ttu-id="468b3-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="468b3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="468b3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="468b3-133">-WhatIf</span></span>
<span data-ttu-id="468b3-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="468b3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="468b3-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="468b3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="468b3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="468b3-136">CommonParameters</span></span>
<span data-ttu-id="468b3-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="468b3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="468b3-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="468b3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="468b3-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="468b3-139">INPUTS</span></span>

### <span data-ttu-id="468b3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="468b3-140">System.String</span></span>

### <span data-ttu-id="468b3-141">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="468b3-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="468b3-142">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="468b3-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="468b3-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="468b3-143">OUTPUTS</span></span>

### <span data-ttu-id="468b3-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="468b3-144">System.Boolean</span></span>

## <span data-ttu-id="468b3-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="468b3-145">NOTES</span></span>

## <span data-ttu-id="468b3-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="468b3-146">RELATED LINKS</span></span>
