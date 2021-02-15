---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 8fbb586e1829cd40302ab290c2d671c67666b7e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115387"
---
# <span data-ttu-id="530a8-101">Add-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="530a8-101">Add-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="530a8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="530a8-102">SYNOPSIS</span></span>
<span data-ttu-id="530a8-103">Adiciona uma regra de rede virtual à conta especificada do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="530a8-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="530a8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="530a8-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="530a8-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="530a8-105">DESCRIPTION</span></span>
<span data-ttu-id="530a8-106">O cmdlet **Add-AzDataLakeStoreVirtualNetworkRule** adiciona uma regra de rede virtual à conta especificada do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="530a8-106">The **Add-AzDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="530a8-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="530a8-107">EXAMPLES</span></span>

### <span data-ttu-id="530a8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="530a8-108">Example 1</span></span>
```powershell
PS C:\> Add-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="530a8-109">Isso cria uma nova regra de rede virtual chamada "myVNET" na conta "dls" com uma id da sub-rede "testId"</span><span class="sxs-lookup"><span data-stu-id="530a8-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="530a8-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="530a8-110">PARAMETERS</span></span>

### <span data-ttu-id="530a8-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="530a8-111">-Account</span></span>
<span data-ttu-id="530a8-112">A conta do Data Lake Store para adicionar a regra de rede virtual</span><span class="sxs-lookup"><span data-stu-id="530a8-112">The Data Lake Store account to add the virtual network rule to</span></span>

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

### <span data-ttu-id="530a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="530a8-113">-DefaultProfile</span></span>
<span data-ttu-id="530a8-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="530a8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="530a8-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="530a8-115">-Name</span></span>
<span data-ttu-id="530a8-116">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="530a8-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="530a8-117">-Sub-RedeId</span><span class="sxs-lookup"><span data-stu-id="530a8-117">-SubnetId</span></span>
<span data-ttu-id="530a8-118">A sub-redeId da regra de rede virtual</span><span class="sxs-lookup"><span data-stu-id="530a8-118">The subnetId of the virtual network rule</span></span>

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

### <span data-ttu-id="530a8-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="530a8-119">-Confirm</span></span>
<span data-ttu-id="530a8-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="530a8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="530a8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="530a8-121">-WhatIf</span></span>
<span data-ttu-id="530a8-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="530a8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="530a8-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="530a8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="530a8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="530a8-124">CommonParameters</span></span>
<span data-ttu-id="530a8-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="530a8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="530a8-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="530a8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="530a8-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="530a8-127">INPUTS</span></span>

### <span data-ttu-id="530a8-128">System.String</span><span class="sxs-lookup"><span data-stu-id="530a8-128">System.String</span></span>

## <span data-ttu-id="530a8-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="530a8-129">OUTPUTS</span></span>

### <span data-ttu-id="530a8-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="530a8-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="530a8-131">Notas</span><span class="sxs-lookup"><span data-stu-id="530a8-131">NOTES</span></span>

## <span data-ttu-id="530a8-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="530a8-132">RELATED LINKS</span></span>
