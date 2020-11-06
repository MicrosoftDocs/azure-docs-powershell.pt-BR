---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 1b404a42c3d40138408d7fb6f2c13a8af91c45c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428484"
---
# <span data-ttu-id="c6352-101">Get-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c6352-101">Get-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="c6352-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6352-102">SYNOPSIS</span></span>
<span data-ttu-id="c6352-103">Obtém as regras de rede virtual especificadas no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="c6352-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="c6352-104">Se nenhuma regra de rede virtual for especificada, lista todas as regras de rede virtual para a conta.</span><span class="sxs-lookup"><span data-stu-id="c6352-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6352-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6352-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6352-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c6352-106">DESCRIPTION</span></span>
<span data-ttu-id="c6352-107">O cmdlet Get-AzureRmDataLakeStoreVirtualNetworkRule Obtém as regras de rede virtual especificadas no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="c6352-107">The Get-AzureRmDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="c6352-108">Se nenhuma regra de rede virtual for especificada, lista todas as regras de rede virtual para a conta.</span><span class="sxs-lookup"><span data-stu-id="c6352-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="c6352-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6352-109">EXAMPLES</span></span>

### <span data-ttu-id="c6352-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c6352-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="c6352-111">Retorna a regra de rede virtual chamada "myVNET" da conta "DLS"</span><span class="sxs-lookup"><span data-stu-id="c6352-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="c6352-112">OS</span><span class="sxs-lookup"><span data-stu-id="c6352-112">PARAMETERS</span></span>

### <span data-ttu-id="c6352-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="c6352-113">-Account</span></span>
<span data-ttu-id="c6352-114">A conta do data Lake Store para a qual obter a regra de rede virtual</span><span class="sxs-lookup"><span data-stu-id="c6352-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="c6352-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6352-115">-DefaultProfile</span></span>
<span data-ttu-id="c6352-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6352-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6352-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c6352-117">-Name</span></span>
<span data-ttu-id="c6352-118">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c6352-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="c6352-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6352-119">CommonParameters</span></span>
<span data-ttu-id="c6352-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6352-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6352-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6352-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6352-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c6352-122">INPUTS</span></span>

### <span data-ttu-id="c6352-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c6352-123">System.String</span></span>

## <span data-ttu-id="c6352-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c6352-124">OUTPUTS</span></span>

### <span data-ttu-id="c6352-125">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c6352-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="c6352-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c6352-126">NOTES</span></span>

## <span data-ttu-id="c6352-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6352-127">RELATED LINKS</span></span>
