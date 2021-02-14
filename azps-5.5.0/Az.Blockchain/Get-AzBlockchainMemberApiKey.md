---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 646d07646ff7530dc805d4c516a1cf981aafe915
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111207"
---
# <span data-ttu-id="3fe19-101">Get-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="3fe19-101">Get-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="3fe19-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3fe19-102">SYNOPSIS</span></span>
<span data-ttu-id="3fe19-103">Lista as chaves da API de um membro da empresa.</span><span class="sxs-lookup"><span data-stu-id="3fe19-103">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="3fe19-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3fe19-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3fe19-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3fe19-105">DESCRIPTION</span></span>
<span data-ttu-id="3fe19-106">Lista as chaves da API de um membro da empresa.</span><span class="sxs-lookup"><span data-stu-id="3fe19-106">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="3fe19-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3fe19-107">EXAMPLES</span></span>

### <span data-ttu-id="3fe19-108">Exemplo 1: List list api keys</span><span class="sxs-lookup"><span data-stu-id="3fe19-108">Example 1: List blockchain Api keys</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

KeyName Value
------- -----
key1    72_8u5HPZJxtZmtvm4Y4W9o-
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="3fe19-109">Este comando lista as chaves da Api de um membro da empresa.</span><span class="sxs-lookup"><span data-stu-id="3fe19-109">This command lists Api keys for a blockchain member.</span></span>

## <span data-ttu-id="3fe19-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3fe19-110">PARAMETERS</span></span>

### <span data-ttu-id="3fe19-111">-OmedoMember</span><span class="sxs-lookup"><span data-stu-id="3fe19-111">-BlockchainMemberName</span></span>
<span data-ttu-id="3fe19-112">Nome do membro Dal med.</span><span class="sxs-lookup"><span data-stu-id="3fe19-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="3fe19-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fe19-113">-DefaultProfile</span></span>
<span data-ttu-id="3fe19-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3fe19-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fe19-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fe19-115">-ResourceGroupName</span></span>
<span data-ttu-id="3fe19-116">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="3fe19-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3fe19-117">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="3fe19-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3fe19-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3fe19-118">-SubscriptionId</span></span>
<span data-ttu-id="3fe19-119">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3fe19-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3fe19-120">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3fe19-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3fe19-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3fe19-121">-Confirm</span></span>
<span data-ttu-id="3fe19-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fe19-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fe19-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fe19-123">-WhatIf</span></span>
<span data-ttu-id="3fe19-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3fe19-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fe19-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3fe19-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fe19-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fe19-126">CommonParameters</span></span>
<span data-ttu-id="3fe19-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fe19-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fe19-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3fe19-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fe19-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="3fe19-129">INPUTS</span></span>

## <span data-ttu-id="3fe19-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="3fe19-130">OUTPUTS</span></span>

### <span data-ttu-id="3fe19-131">Microsoft.Azure.PowerShell.Cmdlets.Bluetooth.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="3fe19-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="3fe19-132">Notas</span><span class="sxs-lookup"><span data-stu-id="3fe19-132">NOTES</span></span>

<span data-ttu-id="3fe19-133">Aliases</span><span class="sxs-lookup"><span data-stu-id="3fe19-133">ALIASES</span></span>

## <span data-ttu-id="3fe19-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3fe19-134">RELATED LINKS</span></span>

