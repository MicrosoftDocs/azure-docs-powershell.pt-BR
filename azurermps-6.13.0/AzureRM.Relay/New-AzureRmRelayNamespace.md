---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
ms.openlocfilehash: a809d563c4fe633669e9b1cf9d3bbb39770bfd85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428396"
---
# <span data-ttu-id="9a47e-101">New-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="9a47e-101">New-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="9a47e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a47e-102">SYNOPSIS</span></span>
<span data-ttu-id="9a47e-103">Cria um novo namespace de transmissão.</span><span class="sxs-lookup"><span data-stu-id="9a47e-103">Creates a new Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a47e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a47e-104">SYNTAX</span></span>

```
New-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a47e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9a47e-105">DESCRIPTION</span></span>
<span data-ttu-id="9a47e-106">O cmdlet **New-AzureRmRelayNamespace** cria um novo namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="9a47e-106">The **New-AzureRmRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="9a47e-107">Uma vez criado, o manifesto do recurso namespace é imutável.</span><span class="sxs-lookup"><span data-stu-id="9a47e-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="9a47e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9a47e-108">EXAMPLES</span></span>

### <span data-ttu-id="9a47e-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9a47e-109">Example 1</span></span>
```
PS C:\> New-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

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

<span data-ttu-id="9a47e-110">Cria um novo namespace de retransmissão dentro do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="9a47e-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="9a47e-111">OS</span><span class="sxs-lookup"><span data-stu-id="9a47e-111">PARAMETERS</span></span>

### <span data-ttu-id="9a47e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a47e-112">-DefaultProfile</span></span>
<span data-ttu-id="9a47e-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9a47e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a47e-114">-Local</span><span class="sxs-lookup"><span data-stu-id="9a47e-114">-Location</span></span>
<span data-ttu-id="9a47e-115">Local do namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="9a47e-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="9a47e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="9a47e-116">-Name</span></span>
<span data-ttu-id="9a47e-117">Nome do namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="9a47e-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="9a47e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a47e-118">-ResourceGroupName</span></span>
<span data-ttu-id="9a47e-119">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9a47e-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="9a47e-120">-Marca</span><span class="sxs-lookup"><span data-stu-id="9a47e-120">-Tag</span></span>
<span data-ttu-id="9a47e-121">Hashtables que representam marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="9a47e-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="9a47e-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9a47e-122">-Confirm</span></span>
<span data-ttu-id="9a47e-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a47e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a47e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a47e-124">-WhatIf</span></span>
<span data-ttu-id="9a47e-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9a47e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a47e-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9a47e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a47e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a47e-127">CommonParameters</span></span>
<span data-ttu-id="9a47e-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a47e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9a47e-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a47e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a47e-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9a47e-130">INPUTS</span></span>

### <span data-ttu-id="9a47e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9a47e-131">System.String</span></span>
<span data-ttu-id="9a47e-132">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9a47e-132">System.Collections.Hashtable</span></span>


## <span data-ttu-id="9a47e-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9a47e-133">OUTPUTS</span></span>

### <span data-ttu-id="9a47e-134">Microsoft. Azure. Commands. Relay. Models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="9a47e-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>


## <span data-ttu-id="9a47e-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9a47e-135">NOTES</span></span>

## <span data-ttu-id="9a47e-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a47e-136">RELATED LINKS</span></span>
