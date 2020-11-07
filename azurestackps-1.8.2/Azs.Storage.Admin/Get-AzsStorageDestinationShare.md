---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0a75fafa646839375bf9dc7f1a64b3084fd31ee4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946888"
---
# <span data-ttu-id="5847e-101">Get-AzsStorageDestinationShare</span><span class="sxs-lookup"><span data-stu-id="5847e-101">Get-AzsStorageDestinationShare</span></span>

## <span data-ttu-id="5847e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5847e-102">SYNOPSIS</span></span>
<span data-ttu-id="5847e-103">Retorna uma lista de compartilhamentos de destino que o sistema considera os melhores candidatos para a migração.</span><span class="sxs-lookup"><span data-stu-id="5847e-103">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="5847e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5847e-104">SYNTAX</span></span>

```
Get-AzsStorageDestinationShare [-SourceShareName] <String> [-FarmName] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="5847e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5847e-105">DESCRIPTION</span></span>
<span data-ttu-id="5847e-106">Retorna uma lista de compartilhamentos de destino que o sistema considera os melhores candidatos para a migração.</span><span class="sxs-lookup"><span data-stu-id="5847e-106">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="5847e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5847e-107">EXAMPLES</span></span>

### <span data-ttu-id="5847e-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="5847e-108">EXAMPLE 1</span></span>
```
Get-AzsStorageDestinationShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -SourceShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="5847e-109">Obtenha uma lista de compartilhamentos de destino que o sistema considera melhores candidatos para a migração.</span><span class="sxs-lookup"><span data-stu-id="5847e-109">Get a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="5847e-110">OS</span><span class="sxs-lookup"><span data-stu-id="5847e-110">PARAMETERS</span></span>

### <span data-ttu-id="5847e-111">-SourceShareName</span><span class="sxs-lookup"><span data-stu-id="5847e-111">-SourceShareName</span></span>
<span data-ttu-id="5847e-112">Nome do compartilhamento que contém os contêineres a serem migrados.</span><span class="sxs-lookup"><span data-stu-id="5847e-112">Name of the share which holds containers to be migrated.</span></span>

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

### <span data-ttu-id="5847e-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="5847e-113">-FarmName</span></span>
<span data-ttu-id="5847e-114">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="5847e-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5847e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5847e-115">-ResourceGroupName</span></span>
<span data-ttu-id="5847e-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5847e-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5847e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5847e-117">CommonParameters</span></span>
<span data-ttu-id="5847e-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5847e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5847e-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5847e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5847e-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5847e-120">INPUTS</span></span>

## <span data-ttu-id="5847e-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5847e-121">OUTPUTS</span></span>

## <span data-ttu-id="5847e-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5847e-122">NOTES</span></span>

## <span data-ttu-id="5847e-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5847e-123">RELATED LINKS</span></span>
