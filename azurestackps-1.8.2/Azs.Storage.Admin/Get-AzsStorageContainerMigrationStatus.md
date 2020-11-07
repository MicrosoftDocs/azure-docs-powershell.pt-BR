---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 96220d7bac0a71f579f81a4d01f4f1dc3cba9dd1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946891"
---
# <span data-ttu-id="87402-101">Get-AzsStorageContainerMigrationStatus</span><span class="sxs-lookup"><span data-stu-id="87402-101">Get-AzsStorageContainerMigrationStatus</span></span>

## <span data-ttu-id="87402-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87402-102">SYNOPSIS</span></span>
<span data-ttu-id="87402-103">Retorna o status de um trabalho de migração de contêineres.</span><span class="sxs-lookup"><span data-stu-id="87402-103">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="87402-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87402-104">SYNTAX</span></span>

```
Get-AzsStorageContainerMigrationStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="87402-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="87402-105">DESCRIPTION</span></span>
<span data-ttu-id="87402-106">Retorna o status de um trabalho de migração de contêineres.</span><span class="sxs-lookup"><span data-stu-id="87402-106">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="87402-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87402-107">EXAMPLES</span></span>

### <span data-ttu-id="87402-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="87402-108">EXAMPLE 1</span></span>
```
Get-AzsStorageContainerMigrationStatus -FarmName "6ed442a3-ec47-4145-b2f0-9b90377b01d0" -JobId "6478ef3b-b7d5-4827-8d47-551c6afb9dd4"
```

<span data-ttu-id="87402-109">Obter o status de um trabalho de migração de contêineres.</span><span class="sxs-lookup"><span data-stu-id="87402-109">Get the status of a container migration job.</span></span>

## <span data-ttu-id="87402-110">OS</span><span class="sxs-lookup"><span data-stu-id="87402-110">PARAMETERS</span></span>

### <span data-ttu-id="87402-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="87402-111">-FarmName</span></span>
<span data-ttu-id="87402-112">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="87402-112">Farm Id.</span></span>

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

### <span data-ttu-id="87402-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="87402-113">-JobId</span></span>
<span data-ttu-id="87402-114">ID da operação.</span><span class="sxs-lookup"><span data-stu-id="87402-114">Operation Id.</span></span>

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

### <span data-ttu-id="87402-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87402-115">-ResourceGroupName</span></span>
<span data-ttu-id="87402-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="87402-116">Resource group name.</span></span>

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

### <span data-ttu-id="87402-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87402-117">CommonParameters</span></span>
<span data-ttu-id="87402-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87402-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87402-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87402-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87402-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="87402-120">INPUTS</span></span>

## <span data-ttu-id="87402-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="87402-121">OUTPUTS</span></span>

### <span data-ttu-id="87402-122">Microsoft. AzureStack. Management. Storage. admin. Models. MigrationResult</span><span class="sxs-lookup"><span data-stu-id="87402-122">Microsoft.AzureStack.Management.Storage.Admin.Models.MigrationResult</span></span>

## <span data-ttu-id="87402-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="87402-123">NOTES</span></span>

## <span data-ttu-id="87402-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87402-124">RELATED LINKS</span></span>
