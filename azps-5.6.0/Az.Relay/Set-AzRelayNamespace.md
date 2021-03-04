---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/set-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
ms.openlocfilehash: 25c633c2929967a5fb580addb78639bff8b6197f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891698"
---
# <span data-ttu-id="7ad1c-101">Set-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="7ad1c-101">Set-AzRelayNamespace</span></span>

## <span data-ttu-id="7ad1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ad1c-102">SYNOPSIS</span></span>
<span data-ttu-id="7ad1c-103">Atualiza a descrição de um namespace Relay existente.</span><span class="sxs-lookup"><span data-stu-id="7ad1c-103">Updates the description of an existing Relay namespace.</span></span>

## <span data-ttu-id="7ad1c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7ad1c-104">SYNTAX</span></span>

```
Set-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ad1c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7ad1c-105">DESCRIPTION</span></span>
<span data-ttu-id="7ad1c-106">O cmdlet **Set-AzRelayNamespace** atualiza a descrição do namespace Relay especificado no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7ad1c-106">The **Set-AzRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="7ad1c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ad1c-107">EXAMPLES</span></span>

### <span data-ttu-id="7ad1c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7ad1c-108">Example 1</span></span>
```
PS C:\> Set-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

ProvisioningState  :
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           :
Location           :
Tags               : {[tag2, Tag2Value]}
Id                 :
Name               :
Type               :
```

<span data-ttu-id="7ad1c-109">Atualiza o namespace Relay com uma nova descrição.</span><span class="sxs-lookup"><span data-stu-id="7ad1c-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="7ad1c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7ad1c-110">PARAMETERS</span></span>

### <span data-ttu-id="7ad1c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ad1c-111">-DefaultProfile</span></span>
<span data-ttu-id="7ad1c-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ad1c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ad1c-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ad1c-113">-InputObject</span></span>
<span data-ttu-id="7ad1c-114">Objeto Namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="7ad1c-114">Relay Namespace object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ad1c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7ad1c-115">-Name</span></span>
<span data-ttu-id="7ad1c-116">Nome do Namespace de Retransmissão.</span><span class="sxs-lookup"><span data-stu-id="7ad1c-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="7ad1c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ad1c-117">-ResourceGroupName</span></span>
<span data-ttu-id="7ad1c-118">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="7ad1c-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="7ad1c-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="7ad1c-119">-Tag</span></span>
<span data-ttu-id="7ad1c-120">Hashtables que representa a marca de recurso.</span><span class="sxs-lookup"><span data-stu-id="7ad1c-120">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="7ad1c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ad1c-121">-Confirm</span></span>
<span data-ttu-id="7ad1c-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ad1c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ad1c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ad1c-123">-WhatIf</span></span>
<span data-ttu-id="7ad1c-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7ad1c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ad1c-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7ad1c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ad1c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ad1c-126">CommonParameters</span></span>
<span data-ttu-id="7ad1c-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ad1c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ad1c-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ad1c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ad1c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ad1c-129">INPUTS</span></span>

### <span data-ttu-id="7ad1c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7ad1c-130">System.String</span></span>

### <span data-ttu-id="7ad1c-131">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7ad1c-131">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7ad1c-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="7ad1c-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>

## <span data-ttu-id="7ad1c-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7ad1c-133">OUTPUTS</span></span>

### <span data-ttu-id="7ad1c-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="7ad1c-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="7ad1c-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="7ad1c-135">NOTES</span></span>

## <span data-ttu-id="7ad1c-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ad1c-136">RELATED LINKS</span></span>
