---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 646d07646ff7530dc805d4c516a1cf981aafe915
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258381"
---
# <span data-ttu-id="0ea65-101">Get-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="0ea65-101">Get-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="0ea65-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0ea65-102">SYNOPSIS</span></span>
<span data-ttu-id="0ea65-103">Lista as chaves de API para um membro de blockchain.</span><span class="sxs-lookup"><span data-stu-id="0ea65-103">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="0ea65-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ea65-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0ea65-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0ea65-105">DESCRIPTION</span></span>
<span data-ttu-id="0ea65-106">Lista as chaves de API para um membro de blockchain.</span><span class="sxs-lookup"><span data-stu-id="0ea65-106">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="0ea65-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0ea65-107">EXAMPLES</span></span>

### <span data-ttu-id="0ea65-108">Exemplo 1: lista as chaves de API blockchain</span><span class="sxs-lookup"><span data-stu-id="0ea65-108">Example 1: List blockchain Api keys</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

KeyName Value
------- -----
key1    72_8u5HPZJxtZmtvm4Y4W9o-
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="0ea65-109">Este comando lista as chaves de API para um membro de blockchain.</span><span class="sxs-lookup"><span data-stu-id="0ea65-109">This command lists Api keys for a blockchain member.</span></span>

## <span data-ttu-id="0ea65-110">OS</span><span class="sxs-lookup"><span data-stu-id="0ea65-110">PARAMETERS</span></span>

### <span data-ttu-id="0ea65-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="0ea65-111">-BlockchainMemberName</span></span>
<span data-ttu-id="0ea65-112">Nome do membro Blockchain.</span><span class="sxs-lookup"><span data-stu-id="0ea65-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="0ea65-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ea65-113">-DefaultProfile</span></span>
<span data-ttu-id="0ea65-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0ea65-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ea65-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ea65-115">-ResourceGroupName</span></span>
<span data-ttu-id="0ea65-116">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="0ea65-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="0ea65-117">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="0ea65-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0ea65-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0ea65-118">-SubscriptionId</span></span>
<span data-ttu-id="0ea65-119">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0ea65-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="0ea65-120">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="0ea65-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0ea65-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0ea65-121">-Confirm</span></span>
<span data-ttu-id="0ea65-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ea65-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ea65-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ea65-123">-WhatIf</span></span>
<span data-ttu-id="0ea65-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0ea65-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ea65-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0ea65-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ea65-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ea65-126">CommonParameters</span></span>
<span data-ttu-id="0ea65-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ea65-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ea65-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ea65-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ea65-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0ea65-129">INPUTS</span></span>

## <span data-ttu-id="0ea65-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0ea65-130">OUTPUTS</span></span>

### <span data-ttu-id="0ea65-131">Microsoft. Azure. PowerShell. cmdlets. Blockchain. Models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="0ea65-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="0ea65-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0ea65-132">NOTES</span></span>

<span data-ttu-id="0ea65-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0ea65-133">ALIASES</span></span>

## <span data-ttu-id="0ea65-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ea65-134">RELATED LINKS</span></span>

