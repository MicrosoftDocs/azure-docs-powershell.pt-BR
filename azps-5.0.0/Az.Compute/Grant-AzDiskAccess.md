---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: 39565aa0675a0afc5f6f3996cad522b435a1a9b2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116808"
---
# <span data-ttu-id="cc497-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="cc497-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="cc497-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc497-102">SYNOPSIS</span></span>
<span data-ttu-id="cc497-103">Concede um acesso a um disco.</span><span class="sxs-lookup"><span data-stu-id="cc497-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="cc497-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc497-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cc497-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc497-105">DESCRIPTION</span></span>
<span data-ttu-id="cc497-106">O cmdlet **Grant-AzDiskAccess** concede um acesso a um disco.</span><span class="sxs-lookup"><span data-stu-id="cc497-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="cc497-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc497-107">EXAMPLES</span></span>

### <span data-ttu-id="cc497-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cc497-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="cc497-109">Conceda o acesso "leitura" ao disco chamado "Disk01" no grupo de recursos chamado "ResourceGroup01" por 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="cc497-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="cc497-110">OS</span><span class="sxs-lookup"><span data-stu-id="cc497-110">PARAMETERS</span></span>

### <span data-ttu-id="cc497-111">-Acesso</span><span class="sxs-lookup"><span data-stu-id="cc497-111">-Access</span></span>
<span data-ttu-id="cc497-112">Especifica o nível de acesso.</span><span class="sxs-lookup"><span data-stu-id="cc497-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="cc497-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc497-113">-AsJob</span></span>
<span data-ttu-id="cc497-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cc497-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc497-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc497-115">-DefaultProfile</span></span>
<span data-ttu-id="cc497-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc497-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc497-117">-Diskname</span><span class="sxs-lookup"><span data-stu-id="cc497-117">-DiskName</span></span>
<span data-ttu-id="cc497-118">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="cc497-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="cc497-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="cc497-119">-DurationInSecond</span></span>
<span data-ttu-id="cc497-120">Especifica a duração do acesso em segundos.</span><span class="sxs-lookup"><span data-stu-id="cc497-120">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="cc497-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc497-121">-ResourceGroupName</span></span>
<span data-ttu-id="cc497-122">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cc497-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cc497-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cc497-123">-Confirm</span></span>
<span data-ttu-id="cc497-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc497-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc497-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc497-125">-WhatIf</span></span>
<span data-ttu-id="cc497-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cc497-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc497-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cc497-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc497-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc497-128">CommonParameters</span></span>
<span data-ttu-id="cc497-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc497-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc497-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc497-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc497-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc497-131">INPUTS</span></span>

### <span data-ttu-id="cc497-132">System. String</span><span class="sxs-lookup"><span data-stu-id="cc497-132">System.String</span></span>

## <span data-ttu-id="cc497-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc497-133">OUTPUTS</span></span>

### <span data-ttu-id="cc497-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="cc497-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="cc497-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc497-135">NOTES</span></span>

## <span data-ttu-id="cc497-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc497-136">RELATED LINKS</span></span>
