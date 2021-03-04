---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 767104edb73265f472e155e8d003b0b5e96906e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886789"
---
# <span data-ttu-id="a4556-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a4556-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="a4556-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4556-102">SYNOPSIS</span></span>
<span data-ttu-id="a4556-103">Revoga um acesso a um disco.</span><span class="sxs-lookup"><span data-stu-id="a4556-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="a4556-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a4556-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4556-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a4556-105">DESCRIPTION</span></span>
<span data-ttu-id="a4556-106">O cmdlet **Revoke-AzDiskAccess** revoga um acesso a um disco.</span><span class="sxs-lookup"><span data-stu-id="a4556-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="a4556-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a4556-107">EXAMPLES</span></span>

### <span data-ttu-id="a4556-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a4556-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="a4556-109">Revogar o acesso ao disco chamado 'Disk01' no grupo de recursos chamado 'ResourceGroup01'</span><span class="sxs-lookup"><span data-stu-id="a4556-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="a4556-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a4556-110">PARAMETERS</span></span>

### <span data-ttu-id="a4556-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4556-111">-AsJob</span></span>
<span data-ttu-id="a4556-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a4556-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4556-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4556-113">-DefaultProfile</span></span>
<span data-ttu-id="a4556-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a4556-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4556-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="a4556-115">-DiskName</span></span>
<span data-ttu-id="a4556-116">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="a4556-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="a4556-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4556-117">-ResourceGroupName</span></span>
<span data-ttu-id="a4556-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a4556-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a4556-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4556-119">-Confirm</span></span>
<span data-ttu-id="a4556-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4556-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4556-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4556-121">-WhatIf</span></span>
<span data-ttu-id="a4556-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a4556-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a4556-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a4556-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4556-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4556-124">CommonParameters</span></span>
<span data-ttu-id="a4556-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4556-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4556-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4556-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4556-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4556-127">INPUTS</span></span>

### <span data-ttu-id="a4556-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a4556-128">System.String</span></span>

## <span data-ttu-id="a4556-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a4556-129">OUTPUTS</span></span>

### <span data-ttu-id="a4556-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a4556-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a4556-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="a4556-131">NOTES</span></span>

## <span data-ttu-id="a4556-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4556-132">RELATED LINKS</span></span>
