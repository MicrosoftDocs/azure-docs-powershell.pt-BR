---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: ee581528810663d09fe724f370b681ff9e20072f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948045"
---
# <span data-ttu-id="9c06f-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="9c06f-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="9c06f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c06f-102">SYNOPSIS</span></span>
<span data-ttu-id="9c06f-103">Remove todos os módulos AzureRm de um computador.</span><span class="sxs-lookup"><span data-stu-id="9c06f-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="9c06f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c06f-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c06f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c06f-105">DESCRIPTION</span></span>
<span data-ttu-id="9c06f-106">Remove todos os módulos AzureRm de um computador.</span><span class="sxs-lookup"><span data-stu-id="9c06f-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="9c06f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c06f-107">EXAMPLES</span></span>

### <span data-ttu-id="9c06f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9c06f-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="9c06f-109">Executar esse comando removerá todos os módulos AzureRm da máquina para a versão do PowerShell em que o cmdlet é executado.</span><span class="sxs-lookup"><span data-stu-id="9c06f-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="9c06f-110">OS</span><span class="sxs-lookup"><span data-stu-id="9c06f-110">PARAMETERS</span></span>

### <span data-ttu-id="9c06f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c06f-111">-DefaultProfile</span></span>
<span data-ttu-id="9c06f-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c06f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c06f-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c06f-113">-PassThru</span></span>
<span data-ttu-id="9c06f-114">Retorne a lista de módulos removidos se especificado.</span><span class="sxs-lookup"><span data-stu-id="9c06f-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="9c06f-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9c06f-115">-Confirm</span></span>
<span data-ttu-id="9c06f-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c06f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c06f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c06f-117">-WhatIf</span></span>
<span data-ttu-id="9c06f-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9c06f-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c06f-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9c06f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c06f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c06f-120">CommonParameters</span></span>
<span data-ttu-id="9c06f-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c06f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c06f-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c06f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c06f-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c06f-123">INPUTS</span></span>

### <span data-ttu-id="9c06f-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9c06f-124">None</span></span>

## <span data-ttu-id="9c06f-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c06f-125">OUTPUTS</span></span>

### <span data-ttu-id="9c06f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9c06f-126">System.String</span></span>

## <span data-ttu-id="9c06f-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c06f-127">NOTES</span></span>

## <span data-ttu-id="9c06f-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c06f-128">RELATED LINKS</span></span>
