---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 196d0eba5119ab984f9ffc632a301d3e65157f63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602956"
---
# <span data-ttu-id="829cc-101">Remove-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="829cc-101">Remove-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="829cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="829cc-102">SYNOPSIS</span></span>
<span data-ttu-id="829cc-103">Remove a regra de rede virtual especificada no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="829cc-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="829cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="829cc-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="829cc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="829cc-105">DESCRIPTION</span></span>
<span data-ttu-id="829cc-106">O cmdlet **Remove-AzureRmDataLakeStoreVirtualNetworkRule** remove a regra de rede virtual especificada no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="829cc-106">The **Remove-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="829cc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="829cc-107">EXAMPLES</span></span>

### <span data-ttu-id="829cc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="829cc-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="829cc-109">Remove a regra de rede virtual "myVNET" da conta "DLS"</span><span class="sxs-lookup"><span data-stu-id="829cc-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="829cc-110">OS</span><span class="sxs-lookup"><span data-stu-id="829cc-110">PARAMETERS</span></span>

### <span data-ttu-id="829cc-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="829cc-111">-Account</span></span>
<span data-ttu-id="829cc-112">A conta do data Lake Store para atualizar a regra de rede virtual no</span><span class="sxs-lookup"><span data-stu-id="829cc-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="829cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="829cc-113">-DefaultProfile</span></span>
<span data-ttu-id="829cc-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="829cc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="829cc-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="829cc-115">-Name</span></span>
<span data-ttu-id="829cc-116">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="829cc-116">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="829cc-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="829cc-117">-PassThru</span></span>
<span data-ttu-id="829cc-118">Indica que uma resposta booliana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="829cc-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="829cc-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="829cc-119">-Confirm</span></span>
<span data-ttu-id="829cc-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="829cc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="829cc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="829cc-121">-WhatIf</span></span>
<span data-ttu-id="829cc-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="829cc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="829cc-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="829cc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="829cc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="829cc-124">CommonParameters</span></span>
<span data-ttu-id="829cc-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="829cc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="829cc-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="829cc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="829cc-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="829cc-127">INPUTS</span></span>

### <span data-ttu-id="829cc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="829cc-128">System.String</span></span>

### <span data-ttu-id="829cc-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="829cc-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="829cc-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="829cc-130">OUTPUTS</span></span>

### <span data-ttu-id="829cc-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="829cc-131">System.Boolean</span></span>

## <span data-ttu-id="829cc-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="829cc-132">NOTES</span></span>

## <span data-ttu-id="829cc-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="829cc-133">RELATED LINKS</span></span>
