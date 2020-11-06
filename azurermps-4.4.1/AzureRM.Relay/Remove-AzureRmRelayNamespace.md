---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
ms.openlocfilehash: d0ac732a0feaffa187ec33d60f9587a7a6a1cff1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440191"
---
# <span data-ttu-id="7d5f1-101">Remove-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="7d5f1-101">Remove-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="7d5f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7d5f1-102">SYNOPSIS</span></span>
<span data-ttu-id="7d5f1-103">Remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="7d5f1-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d5f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d5f1-104">SYNTAX</span></span>

```
Remove-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d5f1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7d5f1-105">DESCRIPTION</span></span>
<span data-ttu-id="7d5f1-106">O cmdlet **Remove-AzureRmRelayNamespace** remove o namespace do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="7d5f1-106">The **Remove-AzureRmRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="7d5f1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d5f1-107">EXAMPLES</span></span>

### <span data-ttu-id="7d5f1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7d5f1-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="7d5f1-109">Remove o namespace de retransmissão `TestNameSpace-Relay1` do grupo de recursos especificado `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="7d5f1-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="7d5f1-110">OS</span><span class="sxs-lookup"><span data-stu-id="7d5f1-110">PARAMETERS</span></span>

### <span data-ttu-id="7d5f1-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d5f1-111">-Name</span></span>
<span data-ttu-id="7d5f1-112">Nome do namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="7d5f1-112">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="7d5f1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d5f1-113">-ResourceGroupName</span></span>
<span data-ttu-id="7d5f1-114">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7d5f1-114">Resource Group Name.</span></span>

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

### <span data-ttu-id="7d5f1-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7d5f1-115">-Confirm</span></span>
<span data-ttu-id="7d5f1-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d5f1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d5f1-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d5f1-117">-WhatIf</span></span>
<span data-ttu-id="7d5f1-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7d5f1-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d5f1-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7d5f1-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d5f1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d5f1-120">-DefaultProfile</span></span>
<span data-ttu-id="7d5f1-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7d5f1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d5f1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d5f1-122">CommonParameters</span></span>
<span data-ttu-id="7d5f1-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d5f1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d5f1-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d5f1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d5f1-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7d5f1-125">INPUTS</span></span>

### <span data-ttu-id="7d5f1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d5f1-126">-ResourceGroupName</span></span>
 <span data-ttu-id="7d5f1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7d5f1-127">System.String</span></span>

### <span data-ttu-id="7d5f1-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d5f1-128">-Name</span></span>
 <span data-ttu-id="7d5f1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7d5f1-129">System.String</span></span>

## <span data-ttu-id="7d5f1-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7d5f1-130">OUTPUTS</span></span>

### <span data-ttu-id="7d5f1-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="7d5f1-131">System.Object</span></span>

## <span data-ttu-id="7d5f1-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7d5f1-132">NOTES</span></span>

## <span data-ttu-id="7d5f1-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d5f1-133">RELATED LINKS</span></span>

