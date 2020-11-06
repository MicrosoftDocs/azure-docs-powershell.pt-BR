---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bdfb3714bbabcacd2805dc4198e2cfffde3f0e8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425632"
---
# <span data-ttu-id="4a2dc-101">New-AzsDataDiskObject</span><span class="sxs-lookup"><span data-stu-id="4a2dc-101">New-AzsDataDiskObject</span></span>

## <span data-ttu-id="4a2dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a2dc-102">SYNOPSIS</span></span>
<span data-ttu-id="4a2dc-103">Cria um disco de dados que é usado para criar uma nova imagem da plataforma da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4a2dc-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="4a2dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a2dc-104">SYNTAX</span></span>

```
New-AzsDataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="4a2dc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4a2dc-105">DESCRIPTION</span></span>
<span data-ttu-id="4a2dc-106">Cria um objeto que contém informações sobre um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="4a2dc-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="4a2dc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a2dc-107">EXAMPLES</span></span>

### <span data-ttu-id="4a2dc-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4a2dc-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsDataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="4a2dc-109">Crie um novo objeto de disco de dados.</span><span class="sxs-lookup"><span data-stu-id="4a2dc-109">Create a new data disk object.</span></span>

## <span data-ttu-id="4a2dc-110">OS</span><span class="sxs-lookup"><span data-stu-id="4a2dc-110">PARAMETERS</span></span>

### <span data-ttu-id="4a2dc-111">-LUN</span><span class="sxs-lookup"><span data-stu-id="4a2dc-111">-Lun</span></span>
<span data-ttu-id="4a2dc-112">Número da unidade lógica.</span><span class="sxs-lookup"><span data-stu-id="4a2dc-112">Logical unit number.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a2dc-113">-URI</span><span class="sxs-lookup"><span data-stu-id="4a2dc-113">-Uri</span></span>
<span data-ttu-id="4a2dc-114">Localização do modelo de disco.</span><span class="sxs-lookup"><span data-stu-id="4a2dc-114">Location of the disk template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a2dc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a2dc-115">CommonParameters</span></span>
<span data-ttu-id="4a2dc-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a2dc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a2dc-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a2dc-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a2dc-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4a2dc-118">INPUTS</span></span>

## <span data-ttu-id="4a2dc-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4a2dc-119">OUTPUTS</span></span>

## <span data-ttu-id="4a2dc-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4a2dc-120">NOTES</span></span>

## <span data-ttu-id="4a2dc-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a2dc-121">RELATED LINKS</span></span>

