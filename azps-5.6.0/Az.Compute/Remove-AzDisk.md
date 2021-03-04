---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
ms.openlocfilehash: c53d49397c79f12500b2a7bbccbec2781f27b610
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887015"
---
# <span data-ttu-id="e1649-101">Remove-AzDisk</span><span class="sxs-lookup"><span data-stu-id="e1649-101">Remove-AzDisk</span></span>

## <span data-ttu-id="e1649-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1649-102">SYNOPSIS</span></span>
<span data-ttu-id="e1649-103">Remove um disco.</span><span class="sxs-lookup"><span data-stu-id="e1649-103">Removes a disk.</span></span>

## <span data-ttu-id="e1649-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e1649-104">SYNTAX</span></span>

```
Remove-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1649-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e1649-105">DESCRIPTION</span></span>
<span data-ttu-id="e1649-106">O cmdlet **Remove-AzDisk** remove um disco.</span><span class="sxs-lookup"><span data-stu-id="e1649-106">The **Remove-AzDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="e1649-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1649-107">EXAMPLES</span></span>

### <span data-ttu-id="e1649-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e1649-108">Example 1</span></span>
```
PS C:\> Remove-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="e1649-109">Este comando remove o disco chamado 'Disk01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="e1649-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e1649-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e1649-110">PARAMETERS</span></span>

### <span data-ttu-id="e1649-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1649-111">-AsJob</span></span>
<span data-ttu-id="e1649-112">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="e1649-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e1649-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1649-113">-DefaultProfile</span></span>
<span data-ttu-id="e1649-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e1649-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1649-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="e1649-115">-DiskName</span></span>
<span data-ttu-id="e1649-116">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="e1649-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="e1649-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e1649-117">-Force</span></span>
<span data-ttu-id="e1649-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e1649-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e1649-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1649-119">-ResourceGroupName</span></span>
<span data-ttu-id="e1649-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e1649-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e1649-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1649-121">-Confirm</span></span>
<span data-ttu-id="e1649-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1649-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1649-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1649-123">-WhatIf</span></span>
<span data-ttu-id="e1649-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e1649-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1649-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e1649-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1649-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1649-126">CommonParameters</span></span>
<span data-ttu-id="e1649-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1649-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1649-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1649-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1649-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1649-129">INPUTS</span></span>

### <span data-ttu-id="e1649-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e1649-130">System.String</span></span>

## <span data-ttu-id="e1649-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e1649-131">OUTPUTS</span></span>

### <span data-ttu-id="e1649-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="e1649-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e1649-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="e1649-133">NOTES</span></span>

## <span data-ttu-id="e1649-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1649-134">RELATED LINKS</span></span>
