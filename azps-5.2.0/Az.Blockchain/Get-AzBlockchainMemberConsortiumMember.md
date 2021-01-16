---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberconsortiummember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
ms.openlocfilehash: f4dc342d72ce092a1f3cbd1695613fce2220661d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259696"
---
# <span data-ttu-id="40db5-101">Get-AzBlockchainMemberConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="40db5-101">Get-AzBlockchainMemberConsortiumMember</span></span>

## <span data-ttu-id="40db5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40db5-102">SYNOPSIS</span></span>
<span data-ttu-id="40db5-103">Lista os membros do consórcio para um membro de blockchain.</span><span class="sxs-lookup"><span data-stu-id="40db5-103">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="40db5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40db5-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="40db5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40db5-105">DESCRIPTION</span></span>
<span data-ttu-id="40db5-106">Lista os membros do consórcio para um membro de blockchain.</span><span class="sxs-lookup"><span data-stu-id="40db5-106">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="40db5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40db5-107">EXAMPLES</span></span>

### <span data-ttu-id="40db5-108">Exemplo 1: lista os membros do consórcio para um membro de blockchain.</span><span class="sxs-lookup"><span data-stu-id="40db5-108">Example 1: Lists the consortium members for a blockchain member.</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

DateModified          DisplayName JoinDate              Name       Role  Status SubscriptionId
------------          ----------- --------              ----       ----  ------ --------------
11/19/2019 5:14:41 AM dolauli001  11/19/2019 5:01:20 AM dolauli001 ADMIN Ready  c9cbd920-c00c-427c-852b-8aaf38badaeb
```

<span data-ttu-id="40db5-109">Esse comando lista os membros do Consortium para um membro blockchain.</span><span class="sxs-lookup"><span data-stu-id="40db5-109">This command lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="40db5-110">OS</span><span class="sxs-lookup"><span data-stu-id="40db5-110">PARAMETERS</span></span>

### <span data-ttu-id="40db5-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="40db5-111">-BlockchainMemberName</span></span>
<span data-ttu-id="40db5-112">Nome do membro Blockchain.</span><span class="sxs-lookup"><span data-stu-id="40db5-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="40db5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40db5-113">-DefaultProfile</span></span>
<span data-ttu-id="40db5-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40db5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40db5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40db5-115">-ResourceGroupName</span></span>
<span data-ttu-id="40db5-116">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="40db5-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="40db5-117">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="40db5-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="40db5-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="40db5-118">-SubscriptionId</span></span>
<span data-ttu-id="40db5-119">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="40db5-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="40db5-120">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="40db5-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="40db5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40db5-121">CommonParameters</span></span>
<span data-ttu-id="40db5-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40db5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40db5-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40db5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40db5-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40db5-124">INPUTS</span></span>

## <span data-ttu-id="40db5-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40db5-125">OUTPUTS</span></span>

### <span data-ttu-id="40db5-126">Microsoft. Azure. PowerShell. cmdlets. Blockchain. Models. Api20180601Preview. IConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="40db5-126">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortiumMember</span></span>

## <span data-ttu-id="40db5-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40db5-127">NOTES</span></span>

<span data-ttu-id="40db5-128">ALIASES</span><span class="sxs-lookup"><span data-stu-id="40db5-128">ALIASES</span></span>

## <span data-ttu-id="40db5-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40db5-129">RELATED LINKS</span></span>

