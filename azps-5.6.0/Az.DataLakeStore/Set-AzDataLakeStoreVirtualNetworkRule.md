---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 98f4dd2a1076df1954674f67829e3ee14da1d871
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891034"
---
# <span data-ttu-id="b68a2-101">Set-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b68a2-101">Set-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="b68a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b68a2-102">SYNOPSIS</span></span>
<span data-ttu-id="b68a2-103">Modifica a regra de rede virtual especificada no Data Lake Store especificado.</span><span class="sxs-lookup"><span data-stu-id="b68a2-103">Modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="b68a2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b68a2-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b68a2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b68a2-105">DESCRIPTION</span></span>
<span data-ttu-id="b68a2-106">O cmdlet **Set-AzDataLakeStoreVirtualNetworkRule** modifica a regra de rede virtual especificada no Repositório de Data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="b68a2-106">The **Set-AzDataLakeStoreVirtualNetworkRule** cmdlet modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="b68a2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b68a2-107">EXAMPLES</span></span>

### <span data-ttu-id="b68a2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b68a2-108">Example 1</span></span>
```powershell
PS C:\> Set-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "updatedId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/updatedId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="b68a2-109">Atualiza a id da sub-rede da regra de rede virtual "myVNET" na conta "dls" para "updatedId"</span><span class="sxs-lookup"><span data-stu-id="b68a2-109">Updates the subnet id of virtual network rule "myVNET" in account "dls" to "updatedId"</span></span>

## <span data-ttu-id="b68a2-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b68a2-110">PARAMETERS</span></span>

### <span data-ttu-id="b68a2-111">-Account</span><span class="sxs-lookup"><span data-stu-id="b68a2-111">-Account</span></span>
<span data-ttu-id="b68a2-112">A conta do Data Lake Store para atualizar a regra de rede virtual em</span><span class="sxs-lookup"><span data-stu-id="b68a2-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="b68a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b68a2-113">-DefaultProfile</span></span>
<span data-ttu-id="b68a2-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b68a2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b68a2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b68a2-115">-Name</span></span>
<span data-ttu-id="b68a2-116">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b68a2-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="b68a2-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b68a2-117">-SubnetId</span></span>
<span data-ttu-id="b68a2-118">O início do intervalo ip válido para a regra de rede virtual</span><span class="sxs-lookup"><span data-stu-id="b68a2-118">The start of the valid ip range for the virtual network rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b68a2-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b68a2-119">-Confirm</span></span>
<span data-ttu-id="b68a2-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b68a2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b68a2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b68a2-121">-WhatIf</span></span>
<span data-ttu-id="b68a2-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b68a2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b68a2-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b68a2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b68a2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b68a2-124">CommonParameters</span></span>
<span data-ttu-id="b68a2-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b68a2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b68a2-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b68a2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b68a2-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b68a2-127">INPUTS</span></span>

### <span data-ttu-id="b68a2-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b68a2-128">System.String</span></span>

## <span data-ttu-id="b68a2-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b68a2-129">OUTPUTS</span></span>

### <span data-ttu-id="b68a2-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b68a2-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="b68a2-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="b68a2-131">NOTES</span></span>

## <span data-ttu-id="b68a2-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b68a2-132">RELATED LINKS</span></span>
