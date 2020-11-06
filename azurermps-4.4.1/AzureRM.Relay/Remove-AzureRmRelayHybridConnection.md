---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 7f65f77d9d1f525dd8850c6934263b608d241751
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433021"
---
# <span data-ttu-id="40bbe-101">Remove-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="40bbe-101">Remove-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="40bbe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40bbe-102">SYNOPSIS</span></span>
<span data-ttu-id="40bbe-103">Remove o HybridConnection do namespace HybridConnection especificado.</span><span class="sxs-lookup"><span data-stu-id="40bbe-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40bbe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40bbe-104">SYNTAX</span></span>

```
Remove-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40bbe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40bbe-105">DESCRIPTION</span></span>
<span data-ttu-id="40bbe-106">O cmdlet **Remove-AzureRmRelayHybridConnection** remove o HybridConnection do namespace de retransmissão especificado.</span><span class="sxs-lookup"><span data-stu-id="40bbe-106">The **Remove-AzureRmRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="40bbe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40bbe-107">EXAMPLES</span></span>

### <span data-ttu-id="40bbe-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="40bbe-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="40bbe-109">Remove o HybridConnection `TestHybridConnection` do namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="40bbe-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="40bbe-110">OS</span><span class="sxs-lookup"><span data-stu-id="40bbe-110">PARAMETERS</span></span>

### <span data-ttu-id="40bbe-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="40bbe-111">-Name</span></span>
<span data-ttu-id="40bbe-112">Nome do HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="40bbe-112">HybridConnections Name.</span></span>

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

### <span data-ttu-id="40bbe-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="40bbe-113">-Namespace</span></span>
<span data-ttu-id="40bbe-114">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="40bbe-114">Namespace Name.</span></span>

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

### <span data-ttu-id="40bbe-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40bbe-115">-ResourceGroupName</span></span>
<span data-ttu-id="40bbe-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="40bbe-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="40bbe-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="40bbe-117">-Confirm</span></span>
<span data-ttu-id="40bbe-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40bbe-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40bbe-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40bbe-119">-WhatIf</span></span>
<span data-ttu-id="40bbe-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="40bbe-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40bbe-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="40bbe-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40bbe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40bbe-122">-DefaultProfile</span></span>
<span data-ttu-id="40bbe-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40bbe-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40bbe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40bbe-124">CommonParameters</span></span>
<span data-ttu-id="40bbe-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40bbe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40bbe-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40bbe-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40bbe-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40bbe-127">INPUTS</span></span>

### <span data-ttu-id="40bbe-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40bbe-128">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="40bbe-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="40bbe-129">-Namespace</span></span>
    System.String

### <span data-ttu-id="40bbe-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="40bbe-130">-Name</span></span>
    System.String

## <span data-ttu-id="40bbe-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40bbe-131">OUTPUTS</span></span>

### <span data-ttu-id="40bbe-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="40bbe-132">System.Object</span></span>

## <span data-ttu-id="40bbe-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40bbe-133">NOTES</span></span>

## <span data-ttu-id="40bbe-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40bbe-134">RELATED LINKS</span></span>
