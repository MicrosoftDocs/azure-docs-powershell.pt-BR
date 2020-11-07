---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: da9fa6503e76d9af8efbdff84ebbcdd501d8232d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775219"
---
# <span data-ttu-id="a9c1d-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="a9c1d-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="a9c1d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9c1d-102">SYNOPSIS</span></span>
<span data-ttu-id="a9c1d-103">Remove todos os módulos AzureRm de um computador.</span><span class="sxs-lookup"><span data-stu-id="a9c1d-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="a9c1d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9c1d-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9c1d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9c1d-105">DESCRIPTION</span></span>
<span data-ttu-id="a9c1d-106">Remove todos os módulos AzureRm de um computador.</span><span class="sxs-lookup"><span data-stu-id="a9c1d-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="a9c1d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9c1d-107">EXAMPLES</span></span>

### <span data-ttu-id="a9c1d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a9c1d-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="a9c1d-109">Executar esse comando removerá todos os módulos AzureRm da máquina para a versão do PowerShell em que o cmdlet é executado.</span><span class="sxs-lookup"><span data-stu-id="a9c1d-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="a9c1d-110">OS</span><span class="sxs-lookup"><span data-stu-id="a9c1d-110">PARAMETERS</span></span>

### <span data-ttu-id="a9c1d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9c1d-111">-DefaultProfile</span></span>
<span data-ttu-id="a9c1d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a9c1d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9c1d-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9c1d-113">-PassThru</span></span>
<span data-ttu-id="a9c1d-114">Retorne a lista de módulos removidos se especificado.</span><span class="sxs-lookup"><span data-stu-id="a9c1d-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="a9c1d-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a9c1d-115">-Confirm</span></span>
<span data-ttu-id="a9c1d-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9c1d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9c1d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9c1d-117">-WhatIf</span></span>
<span data-ttu-id="a9c1d-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a9c1d-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9c1d-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a9c1d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9c1d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9c1d-120">CommonParameters</span></span>
<span data-ttu-id="a9c1d-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9c1d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9c1d-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9c1d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9c1d-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9c1d-123">INPUTS</span></span>

### <span data-ttu-id="a9c1d-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a9c1d-124">None</span></span>

## <span data-ttu-id="a9c1d-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9c1d-125">OUTPUTS</span></span>

### <span data-ttu-id="a9c1d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a9c1d-126">System.String</span></span>

## <span data-ttu-id="a9c1d-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9c1d-127">NOTES</span></span>

## <span data-ttu-id="a9c1d-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9c1d-128">RELATED LINKS</span></span>
