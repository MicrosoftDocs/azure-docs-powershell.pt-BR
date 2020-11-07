---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 401073a8d97affaec866486b19113373c001ae58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955990"
---
# <span data-ttu-id="3ae38-101">Get-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="3ae38-101">Get-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="3ae38-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ae38-102">SYNOPSIS</span></span>
<span data-ttu-id="3ae38-103">Listar as chaves de API do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="3ae38-103">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="3ae38-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ae38-104">SYNTAX</span></span>

```
Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3ae38-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3ae38-105">DESCRIPTION</span></span>
<span data-ttu-id="3ae38-106">Listar as chaves de API do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="3ae38-106">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="3ae38-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ae38-107">EXAMPLES</span></span>

### <span data-ttu-id="3ae38-108">Exemplo 1: listar chaves de API para um nó de transação</span><span class="sxs-lookup"><span data-stu-id="3ae38-108">Example 1: List Api keys for a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001

KeyName Value
------- -----
key1    H4_GPhxbqYENxwas4Vc4l5U9
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="3ae38-109">Esse comando lista as chaves de API para um nó de transação.</span><span class="sxs-lookup"><span data-stu-id="3ae38-109">This command lists Api keys for a transaction node.</span></span>

## <span data-ttu-id="3ae38-110">OS</span><span class="sxs-lookup"><span data-stu-id="3ae38-110">PARAMETERS</span></span>

### <span data-ttu-id="3ae38-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="3ae38-111">-BlockchainMemberName</span></span>
<span data-ttu-id="3ae38-112">Nome do membro Blockchain.</span><span class="sxs-lookup"><span data-stu-id="3ae38-112">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ae38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ae38-113">-DefaultProfile</span></span>
<span data-ttu-id="3ae38-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ae38-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ae38-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ae38-115">-ResourceGroupName</span></span>
<span data-ttu-id="3ae38-116">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="3ae38-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3ae38-117">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="3ae38-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ae38-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ae38-118">-SubscriptionId</span></span>
<span data-ttu-id="3ae38-119">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3ae38-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3ae38-120">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3ae38-120">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ae38-121">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="3ae38-121">-TransactionNodeName</span></span>
<span data-ttu-id="3ae38-122">Nome do nó da transação.</span><span class="sxs-lookup"><span data-stu-id="3ae38-122">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ae38-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3ae38-123">-Confirm</span></span>
<span data-ttu-id="3ae38-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ae38-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ae38-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ae38-125">-WhatIf</span></span>
<span data-ttu-id="3ae38-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3ae38-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ae38-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3ae38-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ae38-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ae38-128">CommonParameters</span></span>
<span data-ttu-id="3ae38-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ae38-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ae38-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ae38-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ae38-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3ae38-131">INPUTS</span></span>

## <span data-ttu-id="3ae38-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3ae38-132">OUTPUTS</span></span>

### <span data-ttu-id="3ae38-133">Microsoft. Azure. PowerShell. cmdlets. Blockchain. Models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="3ae38-133">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="3ae38-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3ae38-134">NOTES</span></span>

<span data-ttu-id="3ae38-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3ae38-135">ALIASES</span></span>

## <span data-ttu-id="3ae38-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ae38-136">RELATED LINKS</span></span>

