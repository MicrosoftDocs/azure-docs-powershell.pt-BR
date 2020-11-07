---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 8fbb586e1829cd40302ab290c2d671c67666b7e3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940519"
---
# <span data-ttu-id="6313d-101">Add-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6313d-101">Add-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="6313d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6313d-102">SYNOPSIS</span></span>
<span data-ttu-id="6313d-103">Adiciona uma regra de rede virtual à conta especificada do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6313d-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="6313d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6313d-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6313d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6313d-105">DESCRIPTION</span></span>
<span data-ttu-id="6313d-106">O cmdlet **Add-AzDataLakeStoreVirtualNetworkRule** adiciona uma regra de rede virtual à conta especificada do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6313d-106">The **Add-AzDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="6313d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6313d-107">EXAMPLES</span></span>

### <span data-ttu-id="6313d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6313d-108">Example 1</span></span>
```powershell
PS C:\> Add-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="6313d-109">Isso cria uma nova regra de rede virtual chamada "myVNET" na conta "DLS" com uma ID de sub-rede "TestId"</span><span class="sxs-lookup"><span data-stu-id="6313d-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="6313d-110">OS</span><span class="sxs-lookup"><span data-stu-id="6313d-110">PARAMETERS</span></span>

### <span data-ttu-id="6313d-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="6313d-111">-Account</span></span>
<span data-ttu-id="6313d-112">A conta do data Lake Store para a qual adicionar a regra de rede virtual</span><span class="sxs-lookup"><span data-stu-id="6313d-112">The Data Lake Store account to add the virtual network rule to</span></span>

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

### <span data-ttu-id="6313d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6313d-113">-DefaultProfile</span></span>
<span data-ttu-id="6313d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6313d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6313d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6313d-115">-Name</span></span>
<span data-ttu-id="6313d-116">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6313d-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="6313d-117">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="6313d-117">-SubnetId</span></span>
<span data-ttu-id="6313d-118">A subnetid da regra de rede virtual</span><span class="sxs-lookup"><span data-stu-id="6313d-118">The subnetId of the virtual network rule</span></span>

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

### <span data-ttu-id="6313d-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6313d-119">-Confirm</span></span>
<span data-ttu-id="6313d-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6313d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6313d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6313d-121">-WhatIf</span></span>
<span data-ttu-id="6313d-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6313d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6313d-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6313d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6313d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6313d-124">CommonParameters</span></span>
<span data-ttu-id="6313d-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6313d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6313d-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6313d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6313d-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6313d-127">INPUTS</span></span>

### <span data-ttu-id="6313d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6313d-128">System.String</span></span>

## <span data-ttu-id="6313d-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6313d-129">OUTPUTS</span></span>

### <span data-ttu-id="6313d-130">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6313d-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="6313d-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6313d-131">NOTES</span></span>

## <span data-ttu-id="6313d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6313d-132">RELATED LINKS</span></span>
