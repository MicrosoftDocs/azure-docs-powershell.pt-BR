---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
ms.openlocfilehash: c243f31ee549443ad959bde13abc9ff3b68c1560
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429134"
---
# <span data-ttu-id="2dbc7-101">Set-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="2dbc7-101">Set-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="2dbc7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2dbc7-102">SYNOPSIS</span></span>
<span data-ttu-id="2dbc7-103">Atualiza a descrição de um namespace de retransmissão existente.</span><span class="sxs-lookup"><span data-stu-id="2dbc7-103">Updates the description of an existing Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dbc7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2dbc7-104">SYNTAX</span></span>

```
Set-AzureRmRelayNamespace [-ResourceGroupName] <String> -Name <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dbc7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2dbc7-105">DESCRIPTION</span></span>
<span data-ttu-id="2dbc7-106">O cmdlet **set-AzureRmRelayNamespace** atualiza a descrição do namespace de retransmissão especificado dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2dbc7-106">The **Set-AzureRmRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="2dbc7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2dbc7-107">EXAMPLES</span></span>

### <span data-ttu-id="2dbc7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2dbc7-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

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

<span data-ttu-id="2dbc7-109">Atualiza o namespace de retransmissão com uma nova descrição.</span><span class="sxs-lookup"><span data-stu-id="2dbc7-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="2dbc7-110">OS</span><span class="sxs-lookup"><span data-stu-id="2dbc7-110">PARAMETERS</span></span>

### <span data-ttu-id="2dbc7-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dbc7-111">-ResourceGroupName</span></span>
<span data-ttu-id="2dbc7-112">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2dbc7-112">Resource Group Name.</span></span>

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

### <span data-ttu-id="2dbc7-113">-Marca</span><span class="sxs-lookup"><span data-stu-id="2dbc7-113">-Tag</span></span>
<span data-ttu-id="2dbc7-114">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2dbc7-114">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2dbc7-115">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="2dbc7-115">For example:</span></span>

<span data-ttu-id="2dbc7-116">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2dbc7-116">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2dbc7-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2dbc7-117">-Confirm</span></span>
<span data-ttu-id="2dbc7-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dbc7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dbc7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dbc7-119">-WhatIf</span></span>
<span data-ttu-id="2dbc7-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2dbc7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dbc7-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2dbc7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dbc7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dbc7-122">-DefaultProfile</span></span>
<span data-ttu-id="2dbc7-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2dbc7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dbc7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2dbc7-124">-InputObject</span></span>
<span data-ttu-id="2dbc7-125">Objeto namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="2dbc7-125">Relay Namespace object.</span></span>

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

### <span data-ttu-id="2dbc7-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="2dbc7-126">-Name</span></span>
<span data-ttu-id="2dbc7-127">Nome do namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="2dbc7-127">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="2dbc7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dbc7-128">CommonParameters</span></span>
<span data-ttu-id="2dbc7-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dbc7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dbc7-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dbc7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dbc7-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2dbc7-131">INPUTS</span></span>

### <span data-ttu-id="2dbc7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dbc7-132">-ResourceGroupName</span></span>
 <span data-ttu-id="2dbc7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2dbc7-133">System.String</span></span>

### <span data-ttu-id="2dbc7-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="2dbc7-134">-NamespaceName</span></span>
 <span data-ttu-id="2dbc7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2dbc7-135">System.String</span></span>

### <span data-ttu-id="2dbc7-136">-Local</span><span class="sxs-lookup"><span data-stu-id="2dbc7-136">-Location</span></span>
 <span data-ttu-id="2dbc7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2dbc7-137">System.String</span></span>

### <span data-ttu-id="2dbc7-138">-Marca</span><span class="sxs-lookup"><span data-stu-id="2dbc7-138">-Tag</span></span>
 <span data-ttu-id="2dbc7-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2dbc7-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2dbc7-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2dbc7-140">OUTPUTS</span></span>

### <span data-ttu-id="2dbc7-141">Microsoft. Azure. Commands. Relay. Models. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="2dbc7-141">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="2dbc7-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2dbc7-142">NOTES</span></span>

## <span data-ttu-id="2dbc7-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2dbc7-143">RELATED LINKS</span></span>

