---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
ms.openlocfilehash: 6076a7fd8a71708bb3bdafdee8f1dfb0650b7088
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114919"
---
# <span data-ttu-id="a4ee4-101">Set-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="a4ee4-101">Set-AzRelayNamespace</span></span>

## <span data-ttu-id="a4ee4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a4ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ee4-103">Atualiza a descrição de um namespace de Retransmissão existente.</span><span class="sxs-lookup"><span data-stu-id="a4ee4-103">Updates the description of an existing Relay namespace.</span></span>

## <span data-ttu-id="a4ee4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4ee4-104">SYNTAX</span></span>

```
Set-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4ee4-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4ee4-105">DESCRIPTION</span></span>
<span data-ttu-id="a4ee4-106">O cmdlet **Set-AzRelayNamespace** atualiza a descrição do namespace de Retransmissão especificado no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a4ee4-106">The **Set-AzRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="a4ee4-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a4ee4-107">EXAMPLES</span></span>

### <span data-ttu-id="a4ee4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a4ee4-108">Example 1</span></span>
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

<span data-ttu-id="a4ee4-109">Atualiza o namespace relay com uma nova descrição.</span><span class="sxs-lookup"><span data-stu-id="a4ee4-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="a4ee4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4ee4-110">PARAMETERS</span></span>

### <span data-ttu-id="a4ee4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ee4-111">-DefaultProfile</span></span>
<span data-ttu-id="a4ee4-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a4ee4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4ee4-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4ee4-113">-InputObject</span></span>
<span data-ttu-id="a4ee4-114">Objeto Namespace de Retransmissão.</span><span class="sxs-lookup"><span data-stu-id="a4ee4-114">Relay Namespace object.</span></span>

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

### <span data-ttu-id="a4ee4-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4ee4-115">-Name</span></span>
<span data-ttu-id="a4ee4-116">Nome do Namespace de Retransmissão.</span><span class="sxs-lookup"><span data-stu-id="a4ee4-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="a4ee4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4ee4-117">-ResourceGroupName</span></span>
<span data-ttu-id="a4ee4-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a4ee4-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="a4ee4-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="a4ee4-119">-Tag</span></span>
<span data-ttu-id="a4ee4-120">Hashtables que representa a marca de recurso.</span><span class="sxs-lookup"><span data-stu-id="a4ee4-120">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="a4ee4-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a4ee4-121">-Confirm</span></span>
<span data-ttu-id="a4ee4-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4ee4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4ee4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4ee4-123">-WhatIf</span></span>
<span data-ttu-id="a4ee4-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a4ee4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4ee4-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a4ee4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4ee4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ee4-126">CommonParameters</span></span>
<span data-ttu-id="a4ee4-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4ee4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ee4-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4ee4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ee4-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="a4ee4-129">INPUTS</span></span>

### <span data-ttu-id="a4ee4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a4ee4-130">System.String</span></span>

### <span data-ttu-id="a4ee4-131">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a4ee4-131">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a4ee4-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="a4ee4-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>

## <span data-ttu-id="a4ee4-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="a4ee4-133">OUTPUTS</span></span>

### <span data-ttu-id="a4ee4-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a4ee4-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="a4ee4-135">Notas</span><span class="sxs-lookup"><span data-stu-id="a4ee4-135">NOTES</span></span>

## <span data-ttu-id="a4ee4-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4ee4-136">RELATED LINKS</span></span>
