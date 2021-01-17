---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 9e455b7160b731f20e5dad6230b2015f73ca5390
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426603"
---
# <span data-ttu-id="d6ca3-101">Remove-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d6ca3-101">Remove-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="d6ca3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="d6ca3-103">Remove a regra de rede virtual especificada no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="d6ca3-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="d6ca3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6ca3-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6ca3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d6ca3-105">DESCRIPTION</span></span>
<span data-ttu-id="d6ca3-106">O cmdlet **Remove-AzDataLakeStoreVirtualNetworkRule** remove a regra de rede virtual especificada no repositório data Lake especificado.</span><span class="sxs-lookup"><span data-stu-id="d6ca3-106">The **Remove-AzDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="d6ca3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6ca3-107">EXAMPLES</span></span>

### <span data-ttu-id="d6ca3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d6ca3-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="d6ca3-109">Remove a regra de rede virtual "myVNET" da conta "DLS"</span><span class="sxs-lookup"><span data-stu-id="d6ca3-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="d6ca3-110">OS</span><span class="sxs-lookup"><span data-stu-id="d6ca3-110">PARAMETERS</span></span>

### <span data-ttu-id="d6ca3-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="d6ca3-111">-Account</span></span>
<span data-ttu-id="d6ca3-112">A conta do data Lake Store para atualizar a regra de rede virtual no</span><span class="sxs-lookup"><span data-stu-id="d6ca3-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="d6ca3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6ca3-113">-DefaultProfile</span></span>
<span data-ttu-id="d6ca3-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6ca3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6ca3-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6ca3-115">-Name</span></span>
<span data-ttu-id="d6ca3-116">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d6ca3-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="d6ca3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6ca3-117">-PassThru</span></span>
<span data-ttu-id="d6ca3-118">Indica que uma resposta booliana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="d6ca3-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="d6ca3-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d6ca3-119">-Confirm</span></span>
<span data-ttu-id="d6ca3-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6ca3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6ca3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6ca3-121">-WhatIf</span></span>
<span data-ttu-id="d6ca3-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d6ca3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6ca3-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d6ca3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6ca3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6ca3-124">CommonParameters</span></span>
<span data-ttu-id="d6ca3-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6ca3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6ca3-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6ca3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6ca3-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d6ca3-127">INPUTS</span></span>

### <span data-ttu-id="d6ca3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d6ca3-128">System.String</span></span>

## <span data-ttu-id="d6ca3-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d6ca3-129">OUTPUTS</span></span>

### <span data-ttu-id="d6ca3-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d6ca3-130">System.Boolean</span></span>

## <span data-ttu-id="d6ca3-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d6ca3-131">NOTES</span></span>

## <span data-ttu-id="d6ca3-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6ca3-132">RELATED LINKS</span></span>
