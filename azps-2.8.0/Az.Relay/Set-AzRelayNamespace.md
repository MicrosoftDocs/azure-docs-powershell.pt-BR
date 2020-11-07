---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
ms.openlocfilehash: eb42dc22f972928405821e8468e5610fa9c4514f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772629"
---
# <span data-ttu-id="2bf7f-101">Set-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="2bf7f-101">Set-AzRelayNamespace</span></span>

## <span data-ttu-id="2bf7f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2bf7f-102">SYNOPSIS</span></span>
<span data-ttu-id="2bf7f-103">Atualiza a descrição de um namespace de retransmissão existente.</span><span class="sxs-lookup"><span data-stu-id="2bf7f-103">Updates the description of an existing Relay namespace.</span></span>

## <span data-ttu-id="2bf7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2bf7f-104">SYNTAX</span></span>

```
Set-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bf7f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2bf7f-105">DESCRIPTION</span></span>
<span data-ttu-id="2bf7f-106">O cmdlet **set-AzRelayNamespace** atualiza a descrição do namespace de retransmissão especificado dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2bf7f-106">The **Set-AzRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="2bf7f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2bf7f-107">EXAMPLES</span></span>

### <span data-ttu-id="2bf7f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2bf7f-108">Example 1</span></span>
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

<span data-ttu-id="2bf7f-109">Atualiza o namespace de retransmissão com uma nova descrição.</span><span class="sxs-lookup"><span data-stu-id="2bf7f-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="2bf7f-110">OS</span><span class="sxs-lookup"><span data-stu-id="2bf7f-110">PARAMETERS</span></span>

### <span data-ttu-id="2bf7f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bf7f-111">-DefaultProfile</span></span>
<span data-ttu-id="2bf7f-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2bf7f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bf7f-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2bf7f-113">-InputObject</span></span>
<span data-ttu-id="2bf7f-114">Objeto namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="2bf7f-114">Relay Namespace object.</span></span>

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

### <span data-ttu-id="2bf7f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2bf7f-115">-Name</span></span>
<span data-ttu-id="2bf7f-116">Nome do namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="2bf7f-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="2bf7f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bf7f-117">-ResourceGroupName</span></span>
<span data-ttu-id="2bf7f-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2bf7f-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="2bf7f-119">-Marca</span><span class="sxs-lookup"><span data-stu-id="2bf7f-119">-Tag</span></span>
<span data-ttu-id="2bf7f-120">Hashtables que representam a marca de recursos.</span><span class="sxs-lookup"><span data-stu-id="2bf7f-120">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="2bf7f-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2bf7f-121">-Confirm</span></span>
<span data-ttu-id="2bf7f-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bf7f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bf7f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bf7f-123">-WhatIf</span></span>
<span data-ttu-id="2bf7f-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2bf7f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bf7f-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2bf7f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bf7f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bf7f-126">CommonParameters</span></span>
<span data-ttu-id="2bf7f-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bf7f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bf7f-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bf7f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bf7f-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2bf7f-129">INPUTS</span></span>

### <span data-ttu-id="2bf7f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2bf7f-130">System.String</span></span>

### <span data-ttu-id="2bf7f-131">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2bf7f-131">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2bf7f-132">Microsoft. Azure. Commands. Relay. Models. RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="2bf7f-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>

## <span data-ttu-id="2bf7f-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2bf7f-133">OUTPUTS</span></span>

### <span data-ttu-id="2bf7f-134">Microsoft. Azure. Commands. Relay. Models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="2bf7f-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="2bf7f-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2bf7f-135">NOTES</span></span>

## <span data-ttu-id="2bf7f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2bf7f-136">RELATED LINKS</span></span>