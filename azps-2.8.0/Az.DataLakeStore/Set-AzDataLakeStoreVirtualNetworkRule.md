---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: ad75f9ea973f80fb68955521a88a11b93fa61890
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596792"
---
# <span data-ttu-id="bc9a9-101">Set-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bc9a9-101">Set-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="bc9a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc9a9-102">SYNOPSIS</span></span>
<span data-ttu-id="bc9a9-103">Modifica a regra de rede virtual especificada no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="bc9a9-103">Modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="bc9a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc9a9-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc9a9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bc9a9-105">DESCRIPTION</span></span>
<span data-ttu-id="bc9a9-106">O cmdlet **set-AzDataLakeStoreVirtualNetworkRule** modifica a regra de rede virtual especificada no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="bc9a9-106">The **Set-AzDataLakeStoreVirtualNetworkRule** cmdlet modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="bc9a9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc9a9-107">EXAMPLES</span></span>

### <span data-ttu-id="bc9a9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bc9a9-108">Example 1</span></span>
```powershell
PS C:\> Set-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "updatedId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/updatedId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="bc9a9-109">Atualiza a identificação de sub-rede da regra de rede virtual "myVNET" na conta "DLS" para "updatedid"</span><span class="sxs-lookup"><span data-stu-id="bc9a9-109">Updates the subnet id of virtual network rule "myVNET" in account "dls" to "updatedId"</span></span>

## <span data-ttu-id="bc9a9-110">OS</span><span class="sxs-lookup"><span data-stu-id="bc9a9-110">PARAMETERS</span></span>

### <span data-ttu-id="bc9a9-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="bc9a9-111">-Account</span></span>
<span data-ttu-id="bc9a9-112">A conta do data Lake Store para atualizar a regra de rede virtual no</span><span class="sxs-lookup"><span data-stu-id="bc9a9-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="bc9a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc9a9-113">-DefaultProfile</span></span>
<span data-ttu-id="bc9a9-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc9a9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc9a9-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc9a9-115">-Name</span></span>
<span data-ttu-id="bc9a9-116">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="bc9a9-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="bc9a9-117">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="bc9a9-117">-SubnetId</span></span>
<span data-ttu-id="bc9a9-118">O início do intervalo de IP válido para a regra de rede virtual</span><span class="sxs-lookup"><span data-stu-id="bc9a9-118">The start of the valid ip range for the virtual network rule</span></span>

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

### <span data-ttu-id="bc9a9-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bc9a9-119">-Confirm</span></span>
<span data-ttu-id="bc9a9-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc9a9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc9a9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc9a9-121">-WhatIf</span></span>
<span data-ttu-id="bc9a9-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bc9a9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc9a9-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bc9a9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc9a9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc9a9-124">CommonParameters</span></span>
<span data-ttu-id="bc9a9-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc9a9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc9a9-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc9a9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc9a9-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bc9a9-127">INPUTS</span></span>

### <span data-ttu-id="bc9a9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="bc9a9-128">System.String</span></span>

## <span data-ttu-id="bc9a9-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bc9a9-129">OUTPUTS</span></span>

### <span data-ttu-id="bc9a9-130">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bc9a9-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="bc9a9-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bc9a9-131">NOTES</span></span>

## <span data-ttu-id="bc9a9-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc9a9-132">RELATED LINKS</span></span>
