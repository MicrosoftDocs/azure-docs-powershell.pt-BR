---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: b05158ae21219760c9c88fe9c0ae3e4978b76f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429567"
---
# <span data-ttu-id="61533-101">Set-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="61533-101">Set-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="61533-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61533-102">SYNOPSIS</span></span>
<span data-ttu-id="61533-103">Modifica a regra de rede virtual especificada no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="61533-103">Modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61533-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61533-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61533-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="61533-105">DESCRIPTION</span></span>
<span data-ttu-id="61533-106">O cmdlet **set-AzureRmDataLakeStoreVirtualNetworkRule** modifica a regra de rede virtual especificada no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="61533-106">The **Set-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="61533-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61533-107">EXAMPLES</span></span>

### <span data-ttu-id="61533-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="61533-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "updatedId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/updatedId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="61533-109">Atualiza a identificação de sub-rede da regra de rede virtual "myVNET" na conta "DLS" para "updatedid"</span><span class="sxs-lookup"><span data-stu-id="61533-109">Updates the subnet id of virtual network rule "myVNET" in account "dls" to "updatedId"</span></span>

## <span data-ttu-id="61533-110">OS</span><span class="sxs-lookup"><span data-stu-id="61533-110">PARAMETERS</span></span>

### <span data-ttu-id="61533-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="61533-111">-Account</span></span>
<span data-ttu-id="61533-112">A conta do data Lake Store para atualizar a regra de rede virtual no</span><span class="sxs-lookup"><span data-stu-id="61533-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="61533-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61533-113">-DefaultProfile</span></span>
<span data-ttu-id="61533-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61533-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61533-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="61533-115">-Name</span></span>
<span data-ttu-id="61533-116">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="61533-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="61533-117">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="61533-117">-SubnetId</span></span>
<span data-ttu-id="61533-118">O início do intervalo de IP válido para a regra de rede virtual</span><span class="sxs-lookup"><span data-stu-id="61533-118">The start of the valid ip range for the virtual network rule</span></span>

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

### <span data-ttu-id="61533-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="61533-119">-Confirm</span></span>
<span data-ttu-id="61533-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61533-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61533-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61533-121">-WhatIf</span></span>
<span data-ttu-id="61533-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="61533-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61533-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="61533-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61533-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61533-124">CommonParameters</span></span>
<span data-ttu-id="61533-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61533-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61533-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61533-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61533-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="61533-127">INPUTS</span></span>

### <span data-ttu-id="61533-128">System. String</span><span class="sxs-lookup"><span data-stu-id="61533-128">System.String</span></span>

## <span data-ttu-id="61533-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="61533-129">OUTPUTS</span></span>

### <span data-ttu-id="61533-130">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="61533-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="61533-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="61533-131">NOTES</span></span>

## <span data-ttu-id="61533-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61533-132">RELATED LINKS</span></span>
