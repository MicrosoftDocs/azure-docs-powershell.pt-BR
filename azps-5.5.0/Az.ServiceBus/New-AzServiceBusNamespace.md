---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
ms.openlocfilehash: 9ef77d9a02f2337aac2886cf033cfa752463e8d2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116181"
---
# <span data-ttu-id="0ad77-101">New-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="0ad77-101">New-AzServiceBusNamespace</span></span>

## <span data-ttu-id="0ad77-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0ad77-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad77-103">Cria um novo namespace de Barra de Serviços.</span><span class="sxs-lookup"><span data-stu-id="0ad77-103">Creates a new Service Bus namespace.</span></span>

## <span data-ttu-id="0ad77-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ad77-104">SYNTAX</span></span>

```
New-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ad77-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ad77-105">DESCRIPTION</span></span>
<span data-ttu-id="0ad77-106">O **cmdlet New-AzServiceBusNamespace** cria um novo namespace de Barra de Serviços.</span><span class="sxs-lookup"><span data-stu-id="0ad77-106">The **New-AzServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="0ad77-107">Depois de criado, o manifesto de recurso namespace é imutável.</span><span class="sxs-lookup"><span data-stu-id="0ad77-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="0ad77-108">Esta operação é idementente.</span><span class="sxs-lookup"><span data-stu-id="0ad77-108">This operation is idempotent.</span></span>

## <span data-ttu-id="0ad77-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0ad77-109">EXAMPLES</span></span>

### <span data-ttu-id="0ad77-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0ad77-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/{SubscriptionId}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="0ad77-111">Cria um novo namespace de Barra de Serviços dentro do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="0ad77-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="0ad77-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ad77-112">PARAMETERS</span></span>

### <span data-ttu-id="0ad77-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad77-113">-DefaultProfile</span></span>
<span data-ttu-id="0ad77-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0ad77-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ad77-115">-Local</span><span class="sxs-lookup"><span data-stu-id="0ad77-115">-Location</span></span>
<span data-ttu-id="0ad77-116">O local de namespace do Barramento de Serviço.</span><span class="sxs-lookup"><span data-stu-id="0ad77-116">The Service Bus namespace location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad77-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ad77-117">-Name</span></span>
<span data-ttu-id="0ad77-118">Nome do Namespace do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="0ad77-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad77-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad77-119">-ResourceGroupName</span></span>
<span data-ttu-id="0ad77-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0ad77-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad77-121">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="0ad77-121">-SkuCapacity</span></span>
<span data-ttu-id="0ad77-122">As unidades de transferência de namespace premium do Service Bus, valores permitidos 1 ou 2 ou 4</span><span class="sxs-lookup"><span data-stu-id="0ad77-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad77-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0ad77-123">-SkuName</span></span>
<span data-ttu-id="0ad77-124">O nome da SKU do namespace de barra de serviços.</span><span class="sxs-lookup"><span data-stu-id="0ad77-124">The Service Bus namespace SKU name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad77-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="0ad77-125">-Tag</span></span>
<span data-ttu-id="0ad77-126">Pares de valor-chave na forma de uma tabela hash definida como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="0ad77-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="0ad77-127">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="0ad77-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad77-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0ad77-128">-Confirm</span></span>
<span data-ttu-id="0ad77-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ad77-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ad77-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ad77-130">-WhatIf</span></span>
<span data-ttu-id="0ad77-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0ad77-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ad77-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0ad77-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ad77-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad77-133">CommonParameters</span></span>
<span data-ttu-id="0ad77-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ad77-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad77-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ad77-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad77-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="0ad77-136">INPUTS</span></span>

### <span data-ttu-id="0ad77-137">System.String</span><span class="sxs-lookup"><span data-stu-id="0ad77-137">System.String</span></span>

### <span data-ttu-id="0ad77-138">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0ad77-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0ad77-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0ad77-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0ad77-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="0ad77-140">OUTPUTS</span></span>

### <span data-ttu-id="0ad77-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="0ad77-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="0ad77-142">Notas</span><span class="sxs-lookup"><span data-stu-id="0ad77-142">NOTES</span></span>

## <span data-ttu-id="0ad77-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ad77-143">RELATED LINKS</span></span>
