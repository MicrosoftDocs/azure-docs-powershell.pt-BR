---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37d41ae2ec772cc755436bc01c3c4009c9c30f5
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774665"
---
# <span data-ttu-id="3788e-101">New-DataDiskObject</span><span class="sxs-lookup"><span data-stu-id="3788e-101">New-DataDiskObject</span></span>

## <span data-ttu-id="3788e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3788e-102">SYNOPSIS</span></span>
<span data-ttu-id="3788e-103">Cria um disco de dados que é usado para criar uma nova imagem da plataforma da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3788e-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="3788e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3788e-104">SYNTAX</span></span>

```
New-DataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="3788e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3788e-105">DESCRIPTION</span></span>
<span data-ttu-id="3788e-106">Cria um objeto que contém informações sobre um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="3788e-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="3788e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3788e-107">EXAMPLES</span></span>

### <span data-ttu-id="3788e-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3788e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-DataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="3788e-109">Crie um novo objeto de disco de dados.</span><span class="sxs-lookup"><span data-stu-id="3788e-109">Create a new data disk object.</span></span>

## <span data-ttu-id="3788e-110">OS</span><span class="sxs-lookup"><span data-stu-id="3788e-110">PARAMETERS</span></span>

### <span data-ttu-id="3788e-111">-LUN</span><span class="sxs-lookup"><span data-stu-id="3788e-111">-Lun</span></span>
<span data-ttu-id="3788e-112">Número da unidade lógica.</span><span class="sxs-lookup"><span data-stu-id="3788e-112">Logical unit number.</span></span>

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

### <span data-ttu-id="3788e-113">-URI</span><span class="sxs-lookup"><span data-stu-id="3788e-113">-Uri</span></span>
<span data-ttu-id="3788e-114">Localização do modelo de disco.</span><span class="sxs-lookup"><span data-stu-id="3788e-114">Location of the disk template.</span></span>

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

### <span data-ttu-id="3788e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3788e-115">CommonParameters</span></span>
<span data-ttu-id="3788e-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3788e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3788e-117">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3788e-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3788e-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3788e-118">INPUTS</span></span>

## <span data-ttu-id="3788e-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3788e-119">OUTPUTS</span></span>

## <span data-ttu-id="3788e-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3788e-120">NOTES</span></span>

## <span data-ttu-id="3788e-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3788e-121">RELATED LINKS</span></span>

