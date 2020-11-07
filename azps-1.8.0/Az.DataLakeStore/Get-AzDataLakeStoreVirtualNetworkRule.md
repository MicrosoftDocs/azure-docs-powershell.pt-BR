---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 079ff61475405407fc2f6864d9fda43b1a5fc4cc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770928"
---
# <span data-ttu-id="e3809-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e3809-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="e3809-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3809-102">SYNOPSIS</span></span>
<span data-ttu-id="e3809-103">Obtém as regras de rede virtual especificadas no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="e3809-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="e3809-104">Se nenhuma regra de rede virtual for especificada, lista todas as regras de rede virtual para a conta.</span><span class="sxs-lookup"><span data-stu-id="e3809-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="e3809-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3809-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3809-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e3809-106">DESCRIPTION</span></span>
<span data-ttu-id="e3809-107">O cmdlet Get-AzDataLakeStoreVirtualNetworkRule Obtém as regras de rede virtual especificadas no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="e3809-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="e3809-108">Se nenhuma regra de rede virtual for especificada, lista todas as regras de rede virtual para a conta.</span><span class="sxs-lookup"><span data-stu-id="e3809-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="e3809-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3809-109">EXAMPLES</span></span>

### <span data-ttu-id="e3809-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e3809-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="e3809-111">Retorna a regra de rede virtual chamada "myVNET" da conta "DLS"</span><span class="sxs-lookup"><span data-stu-id="e3809-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="e3809-112">OS</span><span class="sxs-lookup"><span data-stu-id="e3809-112">PARAMETERS</span></span>

### <span data-ttu-id="e3809-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="e3809-113">-Account</span></span>
<span data-ttu-id="e3809-114">A conta do data Lake Store para a qual obter a regra de rede virtual</span><span class="sxs-lookup"><span data-stu-id="e3809-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="e3809-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3809-115">-DefaultProfile</span></span>
<span data-ttu-id="e3809-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3809-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3809-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3809-117">-Name</span></span>
<span data-ttu-id="e3809-118">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e3809-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="e3809-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3809-119">CommonParameters</span></span>
<span data-ttu-id="e3809-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3809-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3809-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3809-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3809-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e3809-122">INPUTS</span></span>

### <span data-ttu-id="e3809-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e3809-123">System.String</span></span>

## <span data-ttu-id="e3809-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e3809-124">OUTPUTS</span></span>

### <span data-ttu-id="e3809-125">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e3809-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="e3809-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e3809-126">NOTES</span></span>

## <span data-ttu-id="e3809-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3809-127">RELATED LINKS</span></span>
