---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 76fb2e7483bb510d5eceb92b51f7e5e538c3b22b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117835"
---
# <span data-ttu-id="e261f-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="e261f-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="e261f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e261f-102">SYNOPSIS</span></span>
<span data-ttu-id="e261f-103">Revoga um acesso a um disco.</span><span class="sxs-lookup"><span data-stu-id="e261f-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="e261f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e261f-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e261f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e261f-105">DESCRIPTION</span></span>
<span data-ttu-id="e261f-106">O **cmdlet Revoke-AzDiskAccess** revoga um acesso a um disco.</span><span class="sxs-lookup"><span data-stu-id="e261f-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="e261f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e261f-107">EXAMPLES</span></span>

### <span data-ttu-id="e261f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e261f-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="e261f-109">Revogar o acesso ao disco chamado 'Disco01' no grupo de recursos chamado 'ResourceGroup01'</span><span class="sxs-lookup"><span data-stu-id="e261f-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="e261f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e261f-110">PARAMETERS</span></span>

### <span data-ttu-id="e261f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e261f-111">-AsJob</span></span>
<span data-ttu-id="e261f-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e261f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e261f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e261f-113">-DefaultProfile</span></span>
<span data-ttu-id="e261f-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e261f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e261f-115">-Nomedo Disco</span><span class="sxs-lookup"><span data-stu-id="e261f-115">-DiskName</span></span>
<span data-ttu-id="e261f-116">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="e261f-116">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e261f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e261f-117">-ResourceGroupName</span></span>
<span data-ttu-id="e261f-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e261f-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e261f-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e261f-119">-Confirm</span></span>
<span data-ttu-id="e261f-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e261f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e261f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e261f-121">-WhatIf</span></span>
<span data-ttu-id="e261f-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e261f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e261f-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e261f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e261f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e261f-124">CommonParameters</span></span>
<span data-ttu-id="e261f-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e261f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e261f-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e261f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e261f-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="e261f-127">INPUTS</span></span>

### <span data-ttu-id="e261f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e261f-128">System.String</span></span>

## <span data-ttu-id="e261f-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="e261f-129">OUTPUTS</span></span>

### <span data-ttu-id="e261f-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="e261f-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e261f-131">Notas</span><span class="sxs-lookup"><span data-stu-id="e261f-131">NOTES</span></span>

## <span data-ttu-id="e261f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e261f-132">RELATED LINKS</span></span>
