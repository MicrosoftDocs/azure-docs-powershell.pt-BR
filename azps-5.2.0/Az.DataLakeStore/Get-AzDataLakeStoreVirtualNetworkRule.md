---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 95e18d7e36122ed199b4a4c880b4fc918f1164f5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260705"
---
# <span data-ttu-id="d5f1f-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d5f1f-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="d5f1f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="d5f1f-103">Obtém as regras de rede virtual especificadas no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="d5f1f-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="d5f1f-104">Se nenhuma regra de rede virtual for especificada, lista todas as regras de rede virtual para a conta.</span><span class="sxs-lookup"><span data-stu-id="d5f1f-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="d5f1f-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5f1f-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5f1f-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5f1f-106">DESCRIPTION</span></span>
<span data-ttu-id="d5f1f-107">O cmdlet Get-AzDataLakeStoreVirtualNetworkRule Obtém as regras de rede virtual especificadas no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="d5f1f-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="d5f1f-108">Se nenhuma regra de rede virtual for especificada, lista todas as regras de rede virtual para a conta.</span><span class="sxs-lookup"><span data-stu-id="d5f1f-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="d5f1f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5f1f-109">EXAMPLES</span></span>

### <span data-ttu-id="d5f1f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d5f1f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="d5f1f-111">Retorna a regra de rede virtual chamada "myVNET" da conta "DLS"</span><span class="sxs-lookup"><span data-stu-id="d5f1f-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="d5f1f-112">OS</span><span class="sxs-lookup"><span data-stu-id="d5f1f-112">PARAMETERS</span></span>

### <span data-ttu-id="d5f1f-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="d5f1f-113">-Account</span></span>
<span data-ttu-id="d5f1f-114">A conta do data Lake Store para a qual obter a regra de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d5f1f-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="d5f1f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5f1f-115">-DefaultProfile</span></span>
<span data-ttu-id="d5f1f-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5f1f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5f1f-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5f1f-117">-Name</span></span>
<span data-ttu-id="d5f1f-118">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d5f1f-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="d5f1f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5f1f-119">CommonParameters</span></span>
<span data-ttu-id="d5f1f-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5f1f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5f1f-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5f1f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5f1f-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5f1f-122">INPUTS</span></span>

### <span data-ttu-id="d5f1f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d5f1f-123">System.String</span></span>

## <span data-ttu-id="d5f1f-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5f1f-124">OUTPUTS</span></span>

### <span data-ttu-id="d5f1f-125">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d5f1f-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="d5f1f-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5f1f-126">NOTES</span></span>

## <span data-ttu-id="d5f1f-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5f1f-127">RELATED LINKS</span></span>
