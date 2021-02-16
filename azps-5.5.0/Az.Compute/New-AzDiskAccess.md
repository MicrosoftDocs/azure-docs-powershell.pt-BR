---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
ms.openlocfilehash: 430c0d09c56aa4fb57399c97714dc70cb19dd500
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127095"
---
# <span data-ttu-id="4f914-101">New-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="4f914-101">New-AzDiskAccess</span></span>

## <span data-ttu-id="4f914-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f914-102">SYNOPSIS</span></span>
<span data-ttu-id="4f914-103">Cria um recurso de Acesso a Disco</span><span class="sxs-lookup"><span data-stu-id="4f914-103">Creates a Disk Access resource</span></span>

## <span data-ttu-id="4f914-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f914-104">SYNTAX</span></span>

```
New-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f914-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4f914-105">DESCRIPTION</span></span>
<span data-ttu-id="4f914-106">O **cmdlet New-AzDiskAccess cria** um recurso de Acesso a Disco</span><span class="sxs-lookup"><span data-stu-id="4f914-106">The **New-AzDiskAccess** cmdlet creates a Disk Access resource</span></span>

## <span data-ttu-id="4f914-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4f914-107">EXAMPLES</span></span>

### <span data-ttu-id="4f914-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4f914-108">Example 1</span></span>
```
PS C:\> New-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" -Location "NorthCentralUS"
```

<span data-ttu-id="4f914-109">Esse comando criará um Acesso a Disco com determinadas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4f914-109">This command will create a Disk Access with given properties.</span></span> 

## <span data-ttu-id="4f914-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f914-110">PARAMETERS</span></span>

### <span data-ttu-id="4f914-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f914-111">-AsJob</span></span>
<span data-ttu-id="4f914-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4f914-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f914-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f914-113">-DefaultProfile</span></span>
<span data-ttu-id="4f914-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4f914-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f914-115">-Local</span><span class="sxs-lookup"><span data-stu-id="4f914-115">-Location</span></span>
<span data-ttu-id="4f914-116">Especifica o local.</span><span class="sxs-lookup"><span data-stu-id="4f914-116">Specifies the location.</span></span>

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

### <span data-ttu-id="4f914-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="4f914-117">-Name</span></span>
<span data-ttu-id="4f914-118">Especifica o nome de um acesso a disco.</span><span class="sxs-lookup"><span data-stu-id="4f914-118">Specifies the name of a disk access.</span></span>

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

### <span data-ttu-id="4f914-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f914-119">-ResourceGroupName</span></span>
<span data-ttu-id="4f914-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4f914-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4f914-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4f914-121">-Confirm</span></span>
<span data-ttu-id="4f914-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f914-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f914-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f914-123">-WhatIf</span></span>
<span data-ttu-id="4f914-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4f914-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f914-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4f914-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f914-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f914-126">CommonParameters</span></span>
<span data-ttu-id="4f914-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f914-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f914-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f914-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f914-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="4f914-129">INPUTS</span></span>

### <span data-ttu-id="4f914-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4f914-130">System.String</span></span>

## <span data-ttu-id="4f914-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="4f914-131">OUTPUTS</span></span>

### <span data-ttu-id="4f914-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="4f914-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="4f914-133">Notas</span><span class="sxs-lookup"><span data-stu-id="4f914-133">NOTES</span></span>

## <span data-ttu-id="4f914-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f914-134">RELATED LINKS</span></span>
