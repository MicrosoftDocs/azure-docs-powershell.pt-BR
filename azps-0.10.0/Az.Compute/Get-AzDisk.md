---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzDisk.md
ms.openlocfilehash: 1da5ac8a6952e2a03367e84894f2069ba7ff250f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777053"
---
# <span data-ttu-id="0205b-101">Get-AzDisk</span><span class="sxs-lookup"><span data-stu-id="0205b-101">Get-AzDisk</span></span>

## <span data-ttu-id="0205b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0205b-102">SYNOPSIS</span></span>
<span data-ttu-id="0205b-103">Obtém as propriedades de um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="0205b-103">Gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="0205b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0205b-104">SYNTAX</span></span>

```
Get-AzDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0205b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0205b-105">DESCRIPTION</span></span>
<span data-ttu-id="0205b-106">O cmdlet **Get-AzDisk** Obtém as propriedades de um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="0205b-106">The **Get-AzDisk** cmdlet gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="0205b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0205b-107">EXAMPLES</span></span>

### <span data-ttu-id="0205b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0205b-108">Example 1</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="0205b-109">Este comando obtém as propriedades do disco chamado "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="0205b-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="0205b-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0205b-110">Example 2</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="0205b-111">Esse comando obtém as propriedades de todos os discos no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="0205b-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="0205b-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0205b-112">Example 3</span></span>
```
PS C:\> Get-AzDisk
```

<span data-ttu-id="0205b-113">Esse comando obtém as propriedades de todos os discos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="0205b-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="0205b-114">OS</span><span class="sxs-lookup"><span data-stu-id="0205b-114">PARAMETERS</span></span>

### <span data-ttu-id="0205b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0205b-115">-DefaultProfile</span></span>
<span data-ttu-id="0205b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0205b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0205b-117">-Diskname</span><span class="sxs-lookup"><span data-stu-id="0205b-117">-DiskName</span></span>
<span data-ttu-id="0205b-118">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="0205b-118">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0205b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0205b-119">-ResourceGroupName</span></span>
<span data-ttu-id="0205b-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0205b-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0205b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0205b-121">CommonParameters</span></span>
<span data-ttu-id="0205b-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0205b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0205b-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0205b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0205b-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0205b-124">INPUTS</span></span>

### <span data-ttu-id="0205b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0205b-125">System.String</span></span>

## <span data-ttu-id="0205b-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0205b-126">OUTPUTS</span></span>

### <span data-ttu-id="0205b-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="0205b-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="0205b-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0205b-128">NOTES</span></span>

## <span data-ttu-id="0205b-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0205b-129">RELATED LINKS</span></span>

