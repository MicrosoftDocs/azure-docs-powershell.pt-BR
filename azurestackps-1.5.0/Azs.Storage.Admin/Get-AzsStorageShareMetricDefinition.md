---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 646ee96dec361ac6318b4cfe48b80ec4c3686321
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425964"
---
# <span data-ttu-id="61426-101">Get-AzsStorageShareMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="61426-101">Get-AzsStorageShareMetricDefinition</span></span>

## <span data-ttu-id="61426-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61426-102">SYNOPSIS</span></span>
<span data-ttu-id="61426-103">Retorna uma lista de definições de métricas para um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="61426-103">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="61426-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61426-104">SYNTAX</span></span>

```
Get-AzsStorageShareMetricDefinition [-FarmName] <String> [-Name] <String> [[-ResourceGroupName] <String>]
 [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="61426-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="61426-105">DESCRIPTION</span></span>
<span data-ttu-id="61426-106">Retorna uma lista de definições de métricas para um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="61426-106">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="61426-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61426-107">EXAMPLES</span></span>

### <span data-ttu-id="61426-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="61426-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageShareMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Name "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="61426-109">Obter a lista de definições de métrica para um compartilhamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="61426-109">Get the list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="61426-110">OS</span><span class="sxs-lookup"><span data-stu-id="61426-110">PARAMETERS</span></span>

### <span data-ttu-id="61426-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="61426-111">-FarmName</span></span>
<span data-ttu-id="61426-112">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="61426-112">Farm Id.</span></span>

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

### <span data-ttu-id="61426-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="61426-113">-Name</span></span>
<span data-ttu-id="61426-114">Nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="61426-114">Share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61426-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61426-115">-ResourceGroupName</span></span>
<span data-ttu-id="61426-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="61426-116">Resource group name.</span></span>

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

### <span data-ttu-id="61426-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="61426-117">-Skip</span></span>
<span data-ttu-id="61426-118">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="61426-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61426-119">-Início</span><span class="sxs-lookup"><span data-stu-id="61426-119">-Top</span></span>
<span data-ttu-id="61426-120">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="61426-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="61426-121">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="61426-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61426-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61426-122">CommonParameters</span></span>
<span data-ttu-id="61426-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61426-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61426-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61426-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61426-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="61426-125">INPUTS</span></span>

## <span data-ttu-id="61426-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="61426-126">OUTPUTS</span></span>

### <span data-ttu-id="61426-127">Microsoft. AzureStack. Management. Storage. admin. Models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="61426-127">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="61426-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="61426-128">NOTES</span></span>

## <span data-ttu-id="61426-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61426-129">RELATED LINKS</span></span>
