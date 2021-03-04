---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
ms.openlocfilehash: aed0113b229d41665effd7904d2de2357b4b5d93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890445"
---
# <span data-ttu-id="4f626-101">Set-AzDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="4f626-101">Set-AzDiskImageReference</span></span>

## <span data-ttu-id="4f626-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f626-102">SYNOPSIS</span></span>
<span data-ttu-id="4f626-103">Define as propriedades de referência da imagem em um objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="4f626-103">Sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="4f626-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4f626-104">SYNTAX</span></span>

```
Set-AzDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f626-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4f626-105">DESCRIPTION</span></span>
<span data-ttu-id="4f626-106">O cmdlet **Set-AzDiskImageReference** define as propriedades de referência da imagem em um objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="4f626-106">The **Set-AzDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="4f626-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4f626-107">EXAMPLES</span></span>

### <span data-ttu-id="4f626-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4f626-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="4f626-109">O primeiro comando cria um objeto de disco local com tamanho de 10 GB Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4f626-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="4f626-110">Ele também define o tipo de sistema operacional do Windows.</span><span class="sxs-lookup"><span data-stu-id="4f626-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="4f626-111">O segundo comando define a id da imagem e o número da unidade lógica 0 para o objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="4f626-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="4f626-112">O último comando pega o objeto de disco e cria um disco com o nome 'Disk01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="4f626-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4f626-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4f626-113">PARAMETERS</span></span>

### <span data-ttu-id="4f626-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f626-114">-DefaultProfile</span></span>
<span data-ttu-id="4f626-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4f626-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f626-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="4f626-116">-Disk</span></span>
<span data-ttu-id="4f626-117">Especifica um objeto de disco local.</span><span class="sxs-lookup"><span data-stu-id="4f626-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f626-118">-Id</span><span class="sxs-lookup"><span data-stu-id="4f626-118">-Id</span></span>
<span data-ttu-id="4f626-119">Especifica a ID.</span><span class="sxs-lookup"><span data-stu-id="4f626-119">Specifies the ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f626-120">-Lun</span><span class="sxs-lookup"><span data-stu-id="4f626-120">-Lun</span></span>
<span data-ttu-id="4f626-121">Especifica o número da unidade lógica (LUN).</span><span class="sxs-lookup"><span data-stu-id="4f626-121">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f626-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f626-122">-Confirm</span></span>
<span data-ttu-id="4f626-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f626-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f626-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f626-124">-WhatIf</span></span>
<span data-ttu-id="4f626-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4f626-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f626-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4f626-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f626-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f626-127">CommonParameters</span></span>
<span data-ttu-id="4f626-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f626-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f626-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f626-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f626-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4f626-130">INPUTS</span></span>

### <span data-ttu-id="4f626-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="4f626-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="4f626-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4f626-132">System.String</span></span>

### <span data-ttu-id="4f626-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="4f626-133">System.Int32</span></span>

## <span data-ttu-id="4f626-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4f626-134">OUTPUTS</span></span>

### <span data-ttu-id="4f626-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="4f626-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="4f626-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="4f626-136">NOTES</span></span>

## <span data-ttu-id="4f626-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f626-137">RELATED LINKS</span></span>
