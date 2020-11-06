---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
ms.openlocfilehash: 365a80e1ddf5673be5c45c5d17b24490c277a365
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609578"
---
# <span data-ttu-id="20152-101">New-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="20152-101">New-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="20152-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20152-102">SYNOPSIS</span></span>
<span data-ttu-id="20152-103">Cria um novo namespace de transmissão.</span><span class="sxs-lookup"><span data-stu-id="20152-103">Creates a new Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20152-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20152-104">SYNTAX</span></span>

```
New-AzureRmRelayNamespace [-ResourceGroupName] <String> -Name <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20152-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="20152-105">DESCRIPTION</span></span>
<span data-ttu-id="20152-106">O cmdlet **New-AzureRmRelayNamespace** cria um novo namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="20152-106">The **New-AzureRmRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="20152-107">Uma vez criado, o manifesto do recurso namespace é imutável.</span><span class="sxs-lookup"><span data-stu-id="20152-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="20152-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20152-108">EXAMPLES</span></span>

### <span data-ttu-id="20152-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="20152-109">Example 1</span></span>
```
PS C:\> New-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="20152-110">Cria um novo namespace de retransmissão dentro do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="20152-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="20152-111">OS</span><span class="sxs-lookup"><span data-stu-id="20152-111">PARAMETERS</span></span>

### <span data-ttu-id="20152-112">-Local</span><span class="sxs-lookup"><span data-stu-id="20152-112">-Location</span></span>
<span data-ttu-id="20152-113">Local do namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="20152-113">Relay Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20152-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20152-114">-ResourceGroupName</span></span>
<span data-ttu-id="20152-115">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="20152-115">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20152-116">-Marca</span><span class="sxs-lookup"><span data-stu-id="20152-116">-Tag</span></span>
<span data-ttu-id="20152-117">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="20152-117">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="20152-118">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="20152-118">For example:</span></span>

<span data-ttu-id="20152-119">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="20152-119">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="20152-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="20152-120">-Confirm</span></span>
<span data-ttu-id="20152-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20152-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20152-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20152-122">-WhatIf</span></span>
<span data-ttu-id="20152-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="20152-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20152-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="20152-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20152-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20152-125">-DefaultProfile</span></span>
<span data-ttu-id="20152-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20152-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20152-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="20152-127">-Name</span></span>
<span data-ttu-id="20152-128">Nome do namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="20152-128">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20152-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20152-129">CommonParameters</span></span>
<span data-ttu-id="20152-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20152-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20152-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20152-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20152-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="20152-132">INPUTS</span></span>

### <span data-ttu-id="20152-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20152-133">-ResourceGroupName</span></span>
 <span data-ttu-id="20152-134">System. String</span><span class="sxs-lookup"><span data-stu-id="20152-134">System.String</span></span>

### <span data-ttu-id="20152-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="20152-135">-NamespaceName</span></span>
 <span data-ttu-id="20152-136">System. String</span><span class="sxs-lookup"><span data-stu-id="20152-136">System.String</span></span>

### <span data-ttu-id="20152-137">-Local</span><span class="sxs-lookup"><span data-stu-id="20152-137">-Location</span></span>
 <span data-ttu-id="20152-138">System. String</span><span class="sxs-lookup"><span data-stu-id="20152-138">System.String</span></span>

### <span data-ttu-id="20152-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="20152-139">-SkuName</span></span>
 <span data-ttu-id="20152-140">System. String</span><span class="sxs-lookup"><span data-stu-id="20152-140">System.String</span></span>

### <span data-ttu-id="20152-141">-Marca</span><span class="sxs-lookup"><span data-stu-id="20152-141">-Tag</span></span>
 <span data-ttu-id="20152-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="20152-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="20152-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="20152-143">OUTPUTS</span></span>

### <span data-ttu-id="20152-144">Microsoft. Azure. Commands. Relay. Models. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="20152-144">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="20152-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="20152-145">NOTES</span></span>

## <span data-ttu-id="20152-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20152-146">RELATED LINKS</span></span>

