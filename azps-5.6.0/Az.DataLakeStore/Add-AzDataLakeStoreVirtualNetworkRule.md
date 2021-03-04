---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/add-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: e5b6c552d736571acb484ca301372e9eb32d3944
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892504"
---
# <span data-ttu-id="779c9-101">Add-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="779c9-101">Add-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="779c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="779c9-102">SYNOPSIS</span></span>
<span data-ttu-id="779c9-103">Adiciona uma regra de rede virtual à conta especificada do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="779c9-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="779c9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="779c9-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="779c9-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="779c9-105">DESCRIPTION</span></span>
<span data-ttu-id="779c9-106">O cmdlet **Add-AzDataLakeStoreVirtualNetworkRule** adiciona uma regra de rede virtual à conta especificada do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="779c9-106">The **Add-AzDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="779c9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="779c9-107">EXAMPLES</span></span>

### <span data-ttu-id="779c9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="779c9-108">Example 1</span></span>
```powershell
PS C:\> Add-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="779c9-109">Isso cria uma nova regra de rede virtual chamada "myVNET" na conta "dls" com uma id de sub-rede "testId"</span><span class="sxs-lookup"><span data-stu-id="779c9-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="779c9-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="779c9-110">PARAMETERS</span></span>

### <span data-ttu-id="779c9-111">-Account</span><span class="sxs-lookup"><span data-stu-id="779c9-111">-Account</span></span>
<span data-ttu-id="779c9-112">A conta do Data Lake Store para adicionar a regra de rede virtual ao</span><span class="sxs-lookup"><span data-stu-id="779c9-112">The Data Lake Store account to add the virtual network rule to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="779c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="779c9-113">-DefaultProfile</span></span>
<span data-ttu-id="779c9-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="779c9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="779c9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="779c9-115">-Name</span></span>
<span data-ttu-id="779c9-116">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="779c9-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="779c9-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="779c9-117">-SubnetId</span></span>
<span data-ttu-id="779c9-118">A sub-redeId da regra de rede virtual</span><span class="sxs-lookup"><span data-stu-id="779c9-118">The subnetId of the virtual network rule</span></span>

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

### <span data-ttu-id="779c9-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="779c9-119">-Confirm</span></span>
<span data-ttu-id="779c9-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="779c9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="779c9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="779c9-121">-WhatIf</span></span>
<span data-ttu-id="779c9-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="779c9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="779c9-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="779c9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="779c9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="779c9-124">CommonParameters</span></span>
<span data-ttu-id="779c9-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="779c9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="779c9-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="779c9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="779c9-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="779c9-127">INPUTS</span></span>

### <span data-ttu-id="779c9-128">System.String</span><span class="sxs-lookup"><span data-stu-id="779c9-128">System.String</span></span>

## <span data-ttu-id="779c9-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="779c9-129">OUTPUTS</span></span>

### <span data-ttu-id="779c9-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="779c9-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="779c9-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="779c9-131">NOTES</span></span>

## <span data-ttu-id="779c9-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="779c9-132">RELATED LINKS</span></span>
