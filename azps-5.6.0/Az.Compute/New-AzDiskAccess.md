---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
ms.openlocfilehash: 430c0d09c56aa4fb57399c97714dc70cb19dd500
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888997"
---
# <span data-ttu-id="407fa-101">New-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="407fa-101">New-AzDiskAccess</span></span>

## <span data-ttu-id="407fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="407fa-102">SYNOPSIS</span></span>
<span data-ttu-id="407fa-103">Cria um recurso de Acesso ao Disco</span><span class="sxs-lookup"><span data-stu-id="407fa-103">Creates a Disk Access resource</span></span>

## <span data-ttu-id="407fa-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="407fa-104">SYNTAX</span></span>

```
New-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="407fa-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="407fa-105">DESCRIPTION</span></span>
<span data-ttu-id="407fa-106">O cmdlet **New-AzDiskAccess** cria um recurso de Acesso ao Disco</span><span class="sxs-lookup"><span data-stu-id="407fa-106">The **New-AzDiskAccess** cmdlet creates a Disk Access resource</span></span>

## <span data-ttu-id="407fa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="407fa-107">EXAMPLES</span></span>

### <span data-ttu-id="407fa-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="407fa-108">Example 1</span></span>
```
PS C:\> New-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" -Location "NorthCentralUS"
```

<span data-ttu-id="407fa-109">Este comando criará um Acesso em Disco com determinadas propriedades.</span><span class="sxs-lookup"><span data-stu-id="407fa-109">This command will create a Disk Access with given properties.</span></span> 

## <span data-ttu-id="407fa-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="407fa-110">PARAMETERS</span></span>

### <span data-ttu-id="407fa-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="407fa-111">-AsJob</span></span>
<span data-ttu-id="407fa-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="407fa-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="407fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="407fa-113">-DefaultProfile</span></span>
<span data-ttu-id="407fa-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="407fa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="407fa-115">-Location</span><span class="sxs-lookup"><span data-stu-id="407fa-115">-Location</span></span>
<span data-ttu-id="407fa-116">Especifica o local.</span><span class="sxs-lookup"><span data-stu-id="407fa-116">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="407fa-117">-Name</span><span class="sxs-lookup"><span data-stu-id="407fa-117">-Name</span></span>
<span data-ttu-id="407fa-118">Especifica o nome de um acesso em disco.</span><span class="sxs-lookup"><span data-stu-id="407fa-118">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="407fa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="407fa-119">-ResourceGroupName</span></span>
<span data-ttu-id="407fa-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="407fa-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="407fa-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="407fa-121">-Confirm</span></span>
<span data-ttu-id="407fa-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="407fa-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="407fa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="407fa-123">-WhatIf</span></span>
<span data-ttu-id="407fa-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="407fa-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="407fa-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="407fa-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="407fa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="407fa-126">CommonParameters</span></span>
<span data-ttu-id="407fa-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="407fa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="407fa-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="407fa-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="407fa-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="407fa-129">INPUTS</span></span>

### <span data-ttu-id="407fa-130">System.String</span><span class="sxs-lookup"><span data-stu-id="407fa-130">System.String</span></span>

## <span data-ttu-id="407fa-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="407fa-131">OUTPUTS</span></span>

### <span data-ttu-id="407fa-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="407fa-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="407fa-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="407fa-133">NOTES</span></span>

## <span data-ttu-id="407fa-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="407fa-134">RELATED LINKS</span></span>
