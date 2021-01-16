---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 401073a8d97affaec866486b19113373c001ae58
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430383"
---
# <span data-ttu-id="19243-101">Get-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="19243-101">Get-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="19243-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19243-102">SYNOPSIS</span></span>
<span data-ttu-id="19243-103">Listar as chaves de API do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="19243-103">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="19243-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19243-104">SYNTAX</span></span>

```
Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="19243-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19243-105">DESCRIPTION</span></span>
<span data-ttu-id="19243-106">Listar as chaves de API do nó de transação.</span><span class="sxs-lookup"><span data-stu-id="19243-106">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="19243-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19243-107">EXAMPLES</span></span>

### <span data-ttu-id="19243-108">Exemplo 1: listar chaves de API para um nó de transação</span><span class="sxs-lookup"><span data-stu-id="19243-108">Example 1: List Api keys for a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001

KeyName Value
------- -----
key1    H4_GPhxbqYENxwas4Vc4l5U9
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="19243-109">Esse comando lista as chaves de API para um nó de transação.</span><span class="sxs-lookup"><span data-stu-id="19243-109">This command lists Api keys for a transaction node.</span></span>

## <span data-ttu-id="19243-110">OS</span><span class="sxs-lookup"><span data-stu-id="19243-110">PARAMETERS</span></span>

### <span data-ttu-id="19243-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="19243-111">-BlockchainMemberName</span></span>
<span data-ttu-id="19243-112">Nome do membro Blockchain.</span><span class="sxs-lookup"><span data-stu-id="19243-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="19243-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19243-113">-DefaultProfile</span></span>
<span data-ttu-id="19243-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19243-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19243-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19243-115">-ResourceGroupName</span></span>
<span data-ttu-id="19243-116">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="19243-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="19243-117">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="19243-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="19243-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19243-118">-SubscriptionId</span></span>
<span data-ttu-id="19243-119">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="19243-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="19243-120">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="19243-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="19243-121">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="19243-121">-TransactionNodeName</span></span>
<span data-ttu-id="19243-122">Nome do nó da transação.</span><span class="sxs-lookup"><span data-stu-id="19243-122">Transaction node name.</span></span>

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

### <span data-ttu-id="19243-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="19243-123">-Confirm</span></span>
<span data-ttu-id="19243-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19243-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19243-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19243-125">-WhatIf</span></span>
<span data-ttu-id="19243-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="19243-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19243-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="19243-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19243-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19243-128">CommonParameters</span></span>
<span data-ttu-id="19243-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19243-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19243-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19243-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19243-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19243-131">INPUTS</span></span>

## <span data-ttu-id="19243-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19243-132">OUTPUTS</span></span>

### <span data-ttu-id="19243-133">Microsoft. Azure. PowerShell. cmdlets. Blockchain. Models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="19243-133">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="19243-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19243-134">NOTES</span></span>

<span data-ttu-id="19243-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="19243-135">ALIASES</span></span>

## <span data-ttu-id="19243-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19243-136">RELATED LINKS</span></span>

