---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: ec5ac8ab949b95fba3f82ea795dadcecfac360ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888528"
---
# <span data-ttu-id="ae885-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ae885-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="ae885-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae885-102">SYNOPSIS</span></span>
<span data-ttu-id="ae885-103">Obtém as regras de rede virtual especificadas no Data Lake Store especificado.</span><span class="sxs-lookup"><span data-stu-id="ae885-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="ae885-104">Se nenhuma regra de rede virtual for especificada, lista todas as regras de rede virtual da conta.</span><span class="sxs-lookup"><span data-stu-id="ae885-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="ae885-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ae885-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae885-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ae885-106">DESCRIPTION</span></span>
<span data-ttu-id="ae885-107">O Get-AzDataLakeStoreVirtualNetworkRule cmdlet obtém as regras de rede virtual especificadas no Data Lake Store especificado.</span><span class="sxs-lookup"><span data-stu-id="ae885-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="ae885-108">Se nenhuma regra de rede virtual for especificada, lista todas as regras de rede virtual da conta.</span><span class="sxs-lookup"><span data-stu-id="ae885-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="ae885-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae885-109">EXAMPLES</span></span>

### <span data-ttu-id="ae885-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ae885-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="ae885-111">Retorna a regra de rede virtual chamada "myVNET" da conta "dls"</span><span class="sxs-lookup"><span data-stu-id="ae885-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="ae885-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ae885-112">PARAMETERS</span></span>

### <span data-ttu-id="ae885-113">-Account</span><span class="sxs-lookup"><span data-stu-id="ae885-113">-Account</span></span>
<span data-ttu-id="ae885-114">A conta do Data Lake Store para obter a regra de rede virtual de</span><span class="sxs-lookup"><span data-stu-id="ae885-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="ae885-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae885-115">-DefaultProfile</span></span>
<span data-ttu-id="ae885-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae885-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae885-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ae885-117">-Name</span></span>
<span data-ttu-id="ae885-118">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="ae885-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="ae885-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae885-119">CommonParameters</span></span>
<span data-ttu-id="ae885-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae885-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae885-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae885-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae885-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae885-122">INPUTS</span></span>

### <span data-ttu-id="ae885-123">System.String</span><span class="sxs-lookup"><span data-stu-id="ae885-123">System.String</span></span>

## <span data-ttu-id="ae885-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ae885-124">OUTPUTS</span></span>

### <span data-ttu-id="ae885-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ae885-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="ae885-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="ae885-126">NOTES</span></span>

## <span data-ttu-id="ae885-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae885-127">RELATED LINKS</span></span>
