---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: 796690bd0a5774e488b978003c48b02eedaac190
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887272"
---
# <span data-ttu-id="e7319-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="e7319-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="e7319-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7319-102">SYNOPSIS</span></span>
<span data-ttu-id="e7319-103">Remove todos os módulos do AzureRm de um computador.</span><span class="sxs-lookup"><span data-stu-id="e7319-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="e7319-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e7319-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7319-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e7319-105">DESCRIPTION</span></span>
<span data-ttu-id="e7319-106">Remove todos os módulos do AzureRm de um computador.</span><span class="sxs-lookup"><span data-stu-id="e7319-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="e7319-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7319-107">EXAMPLES</span></span>

### <span data-ttu-id="e7319-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e7319-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="e7319-109">Executar esse comando removerá todos os módulos do AzureRm do computador para a versão do PowerShell na qual o cmdlet é executado.</span><span class="sxs-lookup"><span data-stu-id="e7319-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="e7319-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e7319-110">PARAMETERS</span></span>

### <span data-ttu-id="e7319-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7319-111">-DefaultProfile</span></span>
<span data-ttu-id="e7319-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7319-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7319-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7319-113">-PassThru</span></span>
<span data-ttu-id="e7319-114">Retornar lista de Módulos removidos, se especificado.</span><span class="sxs-lookup"><span data-stu-id="e7319-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="e7319-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7319-115">-Confirm</span></span>
<span data-ttu-id="e7319-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7319-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7319-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7319-117">-WhatIf</span></span>
<span data-ttu-id="e7319-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e7319-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7319-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e7319-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7319-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7319-120">CommonParameters</span></span>
<span data-ttu-id="e7319-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7319-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7319-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7319-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7319-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7319-123">INPUTS</span></span>

### <span data-ttu-id="e7319-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e7319-124">None</span></span>

## <span data-ttu-id="e7319-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e7319-125">OUTPUTS</span></span>

### <span data-ttu-id="e7319-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e7319-126">System.String</span></span>

## <span data-ttu-id="e7319-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="e7319-127">NOTES</span></span>

## <span data-ttu-id="e7319-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7319-128">RELATED LINKS</span></span>
