---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: c6f0fc3d8a0ef96a8b54b954e07fb1a9d1c644e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891715"
---
# <span data-ttu-id="c011d-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="c011d-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="c011d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c011d-102">SYNOPSIS</span></span>
<span data-ttu-id="c011d-103">Cria um novo namespace Relay.</span><span class="sxs-lookup"><span data-stu-id="c011d-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="c011d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c011d-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c011d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c011d-105">DESCRIPTION</span></span>
<span data-ttu-id="c011d-106">O cmdlet **New-AzRelayNamespace** cria um novo namespace Relay.</span><span class="sxs-lookup"><span data-stu-id="c011d-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="c011d-107">Depois de criado, o manifesto do recurso namespace é imutável.</span><span class="sxs-lookup"><span data-stu-id="c011d-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="c011d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c011d-108">EXAMPLES</span></span>

### <span data-ttu-id="c011d-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c011d-109">Example 1</span></span>
```
PS C:\> New-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

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

<span data-ttu-id="c011d-110">Cria um novo namespace Relay dentro do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="c011d-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="c011d-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c011d-111">PARAMETERS</span></span>

### <span data-ttu-id="c011d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c011d-112">-DefaultProfile</span></span>
<span data-ttu-id="c011d-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c011d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c011d-114">-Location</span><span class="sxs-lookup"><span data-stu-id="c011d-114">-Location</span></span>
<span data-ttu-id="c011d-115">Local do Namespace de Retransmissão.</span><span class="sxs-lookup"><span data-stu-id="c011d-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="c011d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c011d-116">-Name</span></span>
<span data-ttu-id="c011d-117">Nome do Namespace de Retransmissão.</span><span class="sxs-lookup"><span data-stu-id="c011d-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="c011d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c011d-118">-ResourceGroupName</span></span>
<span data-ttu-id="c011d-119">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="c011d-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="c011d-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="c011d-120">-Tag</span></span>
<span data-ttu-id="c011d-121">Hashtables que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="c011d-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="c011d-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c011d-122">-Confirm</span></span>
<span data-ttu-id="c011d-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c011d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c011d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c011d-124">-WhatIf</span></span>
<span data-ttu-id="c011d-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c011d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c011d-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c011d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c011d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c011d-127">CommonParameters</span></span>
<span data-ttu-id="c011d-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c011d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c011d-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c011d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c011d-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c011d-130">INPUTS</span></span>

### <span data-ttu-id="c011d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c011d-131">System.String</span></span>

### <span data-ttu-id="c011d-132">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c011d-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c011d-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c011d-133">OUTPUTS</span></span>

### <span data-ttu-id="c011d-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c011d-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="c011d-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="c011d-135">NOTES</span></span>

## <span data-ttu-id="c011d-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c011d-136">RELATED LINKS</span></span>
