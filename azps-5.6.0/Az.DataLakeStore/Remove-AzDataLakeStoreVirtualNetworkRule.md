---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: b5b9f154cb494aad7c1ef0faec130b4c4c1cc3d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886675"
---
# <span data-ttu-id="417f6-101">Remove-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="417f6-101">Remove-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="417f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="417f6-102">SYNOPSIS</span></span>
<span data-ttu-id="417f6-103">Remove a regra de rede virtual especificada no Data Lake Store especificado.</span><span class="sxs-lookup"><span data-stu-id="417f6-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="417f6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="417f6-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="417f6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="417f6-105">DESCRIPTION</span></span>
<span data-ttu-id="417f6-106">O cmdlet **Remove-AzDataLakeStoreVirtualNetworkRule** remove a regra de rede virtual especificada no Repositório de Data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="417f6-106">The **Remove-AzDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="417f6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="417f6-107">EXAMPLES</span></span>

### <span data-ttu-id="417f6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="417f6-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="417f6-109">Remove a regra de rede virtual "myVNET" da conta "dls"</span><span class="sxs-lookup"><span data-stu-id="417f6-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="417f6-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="417f6-110">PARAMETERS</span></span>

### <span data-ttu-id="417f6-111">-Account</span><span class="sxs-lookup"><span data-stu-id="417f6-111">-Account</span></span>
<span data-ttu-id="417f6-112">A conta do Data Lake Store para atualizar a regra de rede virtual em</span><span class="sxs-lookup"><span data-stu-id="417f6-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="417f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="417f6-113">-DefaultProfile</span></span>
<span data-ttu-id="417f6-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="417f6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="417f6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="417f6-115">-Name</span></span>
<span data-ttu-id="417f6-116">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="417f6-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="417f6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="417f6-117">-PassThru</span></span>
<span data-ttu-id="417f6-118">Indica que uma resposta booleana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="417f6-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="417f6-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="417f6-119">-Confirm</span></span>
<span data-ttu-id="417f6-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="417f6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="417f6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="417f6-121">-WhatIf</span></span>
<span data-ttu-id="417f6-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="417f6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="417f6-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="417f6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="417f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="417f6-124">CommonParameters</span></span>
<span data-ttu-id="417f6-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="417f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="417f6-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="417f6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="417f6-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="417f6-127">INPUTS</span></span>

### <span data-ttu-id="417f6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="417f6-128">System.String</span></span>

## <span data-ttu-id="417f6-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="417f6-129">OUTPUTS</span></span>

### <span data-ttu-id="417f6-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="417f6-130">System.Boolean</span></span>

## <span data-ttu-id="417f6-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="417f6-131">NOTES</span></span>

## <span data-ttu-id="417f6-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="417f6-132">RELATED LINKS</span></span>
