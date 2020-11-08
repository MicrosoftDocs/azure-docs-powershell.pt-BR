---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
ms.openlocfilehash: 430c0d09c56aa4fb57399c97714dc70cb19dd500
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113118"
---
# <span data-ttu-id="4998b-101">New-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="4998b-101">New-AzDiskAccess</span></span>

## <span data-ttu-id="4998b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4998b-102">SYNOPSIS</span></span>
<span data-ttu-id="4998b-103">Cria um recurso de acesso a disco</span><span class="sxs-lookup"><span data-stu-id="4998b-103">Creates a Disk Access resource</span></span>

## <span data-ttu-id="4998b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4998b-104">SYNTAX</span></span>

```
New-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4998b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4998b-105">DESCRIPTION</span></span>
<span data-ttu-id="4998b-106">O cmdlet **New-AzDiskAccess** cria um recurso de acesso a disco</span><span class="sxs-lookup"><span data-stu-id="4998b-106">The **New-AzDiskAccess** cmdlet creates a Disk Access resource</span></span>

## <span data-ttu-id="4998b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4998b-107">EXAMPLES</span></span>

### <span data-ttu-id="4998b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4998b-108">Example 1</span></span>
```
PS C:\> New-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" -Location "NorthCentralUS"
```

<span data-ttu-id="4998b-109">Esse comando criará um acesso a disco com as propriedades fornecidas.</span><span class="sxs-lookup"><span data-stu-id="4998b-109">This command will create a Disk Access with given properties.</span></span> 

## <span data-ttu-id="4998b-110">OS</span><span class="sxs-lookup"><span data-stu-id="4998b-110">PARAMETERS</span></span>

### <span data-ttu-id="4998b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4998b-111">-AsJob</span></span>
<span data-ttu-id="4998b-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4998b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4998b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4998b-113">-DefaultProfile</span></span>
<span data-ttu-id="4998b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4998b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4998b-115">-Local</span><span class="sxs-lookup"><span data-stu-id="4998b-115">-Location</span></span>
<span data-ttu-id="4998b-116">Especifica o local.</span><span class="sxs-lookup"><span data-stu-id="4998b-116">Specifies the location.</span></span>

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

### <span data-ttu-id="4998b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="4998b-117">-Name</span></span>
<span data-ttu-id="4998b-118">Especifica o nome de um acesso a disco.</span><span class="sxs-lookup"><span data-stu-id="4998b-118">Specifies the name of a disk access.</span></span>

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

### <span data-ttu-id="4998b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4998b-119">-ResourceGroupName</span></span>
<span data-ttu-id="4998b-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4998b-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4998b-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4998b-121">-Confirm</span></span>
<span data-ttu-id="4998b-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4998b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4998b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4998b-123">-WhatIf</span></span>
<span data-ttu-id="4998b-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4998b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4998b-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4998b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4998b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4998b-126">CommonParameters</span></span>
<span data-ttu-id="4998b-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4998b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4998b-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4998b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4998b-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4998b-129">INPUTS</span></span>

### <span data-ttu-id="4998b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4998b-130">System.String</span></span>

## <span data-ttu-id="4998b-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4998b-131">OUTPUTS</span></span>

### <span data-ttu-id="4998b-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="4998b-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="4998b-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4998b-133">NOTES</span></span>

## <span data-ttu-id="4998b-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4998b-134">RELATED LINKS</span></span>
