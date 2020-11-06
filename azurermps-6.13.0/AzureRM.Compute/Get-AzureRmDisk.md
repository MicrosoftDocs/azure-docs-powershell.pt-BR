---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: 00d7368c49c86a9c089fef5bce3698b32eb65a74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428570"
---
# <span data-ttu-id="e1fc3-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="e1fc3-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="e1fc3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e1fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="e1fc3-103">Obtém as propriedades de um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-103">Gets the properties of a Managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1fc3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1fc3-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1fc3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e1fc3-105">DESCRIPTION</span></span>
<span data-ttu-id="e1fc3-106">O cmdlet **Get-AzureRmDisk** Obtém as propriedades de um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-106">The **Get-AzureRmDisk** cmdlet gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="e1fc3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1fc3-107">EXAMPLES</span></span>

### <span data-ttu-id="e1fc3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e1fc3-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="e1fc3-109">Este comando obtém as propriedades do disco chamado "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e1fc3-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="e1fc3-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e1fc3-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="e1fc3-111">Esse comando obtém as propriedades de todos os discos no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e1fc3-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="e1fc3-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e1fc3-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="e1fc3-113">Esse comando obtém as propriedades de todos os discos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="e1fc3-114">OS</span><span class="sxs-lookup"><span data-stu-id="e1fc3-114">PARAMETERS</span></span>

### <span data-ttu-id="e1fc3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1fc3-115">-DefaultProfile</span></span>
<span data-ttu-id="e1fc3-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1fc3-117">-Diskname</span><span class="sxs-lookup"><span data-stu-id="e1fc3-117">-DiskName</span></span>
<span data-ttu-id="e1fc3-118">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-118">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1fc3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1fc3-119">-ResourceGroupName</span></span>
<span data-ttu-id="e1fc3-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e1fc3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1fc3-121">CommonParameters</span></span>
<span data-ttu-id="e1fc3-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1fc3-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1fc3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1fc3-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e1fc3-124">INPUTS</span></span>

### <span data-ttu-id="e1fc3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e1fc3-125">System.String</span></span>

## <span data-ttu-id="e1fc3-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e1fc3-126">OUTPUTS</span></span>

### <span data-ttu-id="e1fc3-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="e1fc3-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="e1fc3-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e1fc3-128">NOTES</span></span>

## <span data-ttu-id="e1fc3-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1fc3-129">RELATED LINKS</span></span>
