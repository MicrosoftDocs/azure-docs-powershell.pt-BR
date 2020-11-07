---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0fb6da4bde577d5a69c5bd85261822e3cf1865d
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775071"
---
# <span data-ttu-id="c873b-101">Get-AzsBlobService</span><span class="sxs-lookup"><span data-stu-id="c873b-101">Get-AzsBlobService</span></span>

## <span data-ttu-id="c873b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c873b-102">SYNOPSIS</span></span>
<span data-ttu-id="c873b-103">Retorna o serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="c873b-103">Returns the blob service.</span></span>

## <span data-ttu-id="c873b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c873b-104">SYNTAX</span></span>

```
Get-AzsBlobService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="c873b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c873b-105">DESCRIPTION</span></span>
<span data-ttu-id="c873b-106">Retorna o serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="c873b-106">Returns the blob service.</span></span>

## <span data-ttu-id="c873b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c873b-107">EXAMPLES</span></span>

### <span data-ttu-id="c873b-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="c873b-108">EXAMPLE 1</span></span>
```
Get-AzsBlobService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="c873b-109">Obter o serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="c873b-109">Get the blob service.</span></span>

## <span data-ttu-id="c873b-110">OS</span><span class="sxs-lookup"><span data-stu-id="c873b-110">PARAMETERS</span></span>

### <span data-ttu-id="c873b-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="c873b-111">-FarmName</span></span>
<span data-ttu-id="c873b-112">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="c873b-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c873b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c873b-113">-ResourceGroupName</span></span>
<span data-ttu-id="c873b-114">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c873b-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c873b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c873b-115">CommonParameters</span></span>
<span data-ttu-id="c873b-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c873b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c873b-117">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c873b-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c873b-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c873b-118">INPUTS</span></span>

## <span data-ttu-id="c873b-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c873b-119">OUTPUTS</span></span>

### <span data-ttu-id="c873b-120">Microsoft. AzureStack. Management. Storage. admin. Models. BlobService</span><span class="sxs-lookup"><span data-stu-id="c873b-120">Microsoft.AzureStack.Management.Storage.Admin.Models.BlobService</span></span>

## <span data-ttu-id="c873b-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c873b-121">NOTES</span></span>

## <span data-ttu-id="c873b-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c873b-122">RELATED LINKS</span></span>