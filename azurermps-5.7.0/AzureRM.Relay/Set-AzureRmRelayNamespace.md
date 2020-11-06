---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
ms.openlocfilehash: 09c601e2ecfddf417e90efd60b58bcdd1a51ff5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428807"
---
# <span data-ttu-id="f53d1-101">Set-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="f53d1-101">Set-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="f53d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f53d1-102">SYNOPSIS</span></span>
<span data-ttu-id="f53d1-103">Atualiza a descrição de um namespace de retransmissão existente.</span><span class="sxs-lookup"><span data-stu-id="f53d1-103">Updates the description of an existing Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f53d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f53d1-104">SYNTAX</span></span>

```
Set-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f53d1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f53d1-105">DESCRIPTION</span></span>
<span data-ttu-id="f53d1-106">O cmdlet **set-AzureRmRelayNamespace** atualiza a descrição do namespace de retransmissão especificado dentro do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f53d1-106">The **Set-AzureRmRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="f53d1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f53d1-107">EXAMPLES</span></span>

### <span data-ttu-id="f53d1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f53d1-108">Example 1</span></span>
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

<span data-ttu-id="f53d1-109">Atualiza o namespace de retransmissão com uma nova descrição.</span><span class="sxs-lookup"><span data-stu-id="f53d1-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="f53d1-110">OS</span><span class="sxs-lookup"><span data-stu-id="f53d1-110">PARAMETERS</span></span>

### <span data-ttu-id="f53d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f53d1-111">-DefaultProfile</span></span>
<span data-ttu-id="f53d1-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f53d1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53d1-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f53d1-113">-InputObject</span></span>
<span data-ttu-id="f53d1-114">Objeto namespace de retransmissão</span><span class="sxs-lookup"><span data-stu-id="f53d1-114">Relay Namespace object</span></span>

```yaml
Type: RelayNamespaceAttirbutesUpdateParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f53d1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f53d1-115">-Name</span></span>
<span data-ttu-id="f53d1-116">Nome do namespace de retransmissão</span><span class="sxs-lookup"><span data-stu-id="f53d1-116">Relay Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f53d1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f53d1-117">-ResourceGroupName</span></span>
<span data-ttu-id="f53d1-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f53d1-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f53d1-119">-Marca</span><span class="sxs-lookup"><span data-stu-id="f53d1-119">-Tag</span></span>
<span data-ttu-id="f53d1-120">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f53d1-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f53d1-121">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f53d1-121">For example:</span></span>

<span data-ttu-id="f53d1-122">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f53d1-122">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f53d1-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f53d1-123">-Confirm</span></span>
<span data-ttu-id="f53d1-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f53d1-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53d1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f53d1-125">-WhatIf</span></span>
<span data-ttu-id="f53d1-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f53d1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f53d1-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f53d1-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53d1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f53d1-128">CommonParameters</span></span>
<span data-ttu-id="f53d1-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f53d1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f53d1-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f53d1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f53d1-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f53d1-131">INPUTS</span></span>

### <span data-ttu-id="f53d1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f53d1-132">-ResourceGroupName</span></span>
 <span data-ttu-id="f53d1-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f53d1-133">System.String</span></span>

### <span data-ttu-id="f53d1-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f53d1-134">-NamespaceName</span></span>
 <span data-ttu-id="f53d1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f53d1-135">System.String</span></span>

### <span data-ttu-id="f53d1-136">-Local</span><span class="sxs-lookup"><span data-stu-id="f53d1-136">-Location</span></span>
 <span data-ttu-id="f53d1-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f53d1-137">System.String</span></span>

### <span data-ttu-id="f53d1-138">-Marca</span><span class="sxs-lookup"><span data-stu-id="f53d1-138">-Tag</span></span>
 <span data-ttu-id="f53d1-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f53d1-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f53d1-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f53d1-140">OUTPUTS</span></span>

### <span data-ttu-id="f53d1-141">Microsoft. Azure. Commands. Relay. Models. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="f53d1-141">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="f53d1-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f53d1-142">NOTES</span></span>

## <span data-ttu-id="f53d1-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f53d1-143">RELATED LINKS</span></span>

