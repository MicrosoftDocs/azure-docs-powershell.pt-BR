---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: 39565aa0675a0afc5f6f3996cad522b435a1a9b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127097"
---
# <span data-ttu-id="d04f6-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="d04f6-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="d04f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d04f6-102">SYNOPSIS</span></span>
<span data-ttu-id="d04f6-103">Concede acesso a um disco.</span><span class="sxs-lookup"><span data-stu-id="d04f6-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="d04f6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d04f6-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d04f6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d04f6-105">DESCRIPTION</span></span>
<span data-ttu-id="d04f6-106">O cmdlet **Grant-AzDiskAccess** concede acesso a um disco.</span><span class="sxs-lookup"><span data-stu-id="d04f6-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="d04f6-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d04f6-107">EXAMPLES</span></span>

### <span data-ttu-id="d04f6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d04f6-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="d04f6-109">Conceda acesso de 'Leitura' ao disco chamado 'Disco01' no grupo de recursos chamado 'ResourceGroup01' por 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="d04f6-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="d04f6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d04f6-110">PARAMETERS</span></span>

### <span data-ttu-id="d04f6-111">-Access</span><span class="sxs-lookup"><span data-stu-id="d04f6-111">-Access</span></span>
<span data-ttu-id="d04f6-112">Especifica o nível do Access.</span><span class="sxs-lookup"><span data-stu-id="d04f6-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d04f6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d04f6-113">-AsJob</span></span>
<span data-ttu-id="d04f6-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d04f6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d04f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d04f6-115">-DefaultProfile</span></span>
<span data-ttu-id="d04f6-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d04f6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d04f6-117">-Nomedo Disco</span><span class="sxs-lookup"><span data-stu-id="d04f6-117">-DiskName</span></span>
<span data-ttu-id="d04f6-118">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="d04f6-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="d04f6-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="d04f6-119">-DurationInSecond</span></span>
<span data-ttu-id="d04f6-120">Especifica a duração do acesso em segundos.</span><span class="sxs-lookup"><span data-stu-id="d04f6-120">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d04f6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d04f6-121">-ResourceGroupName</span></span>
<span data-ttu-id="d04f6-122">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d04f6-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d04f6-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d04f6-123">-Confirm</span></span>
<span data-ttu-id="d04f6-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d04f6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d04f6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d04f6-125">-WhatIf</span></span>
<span data-ttu-id="d04f6-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d04f6-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d04f6-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d04f6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d04f6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d04f6-128">CommonParameters</span></span>
<span data-ttu-id="d04f6-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d04f6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d04f6-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d04f6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d04f6-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="d04f6-131">INPUTS</span></span>

### <span data-ttu-id="d04f6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d04f6-132">System.String</span></span>

## <span data-ttu-id="d04f6-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="d04f6-133">OUTPUTS</span></span>

### <span data-ttu-id="d04f6-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="d04f6-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="d04f6-135">Notas</span><span class="sxs-lookup"><span data-stu-id="d04f6-135">NOTES</span></span>

## <span data-ttu-id="d04f6-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d04f6-136">RELATED LINKS</span></span>
